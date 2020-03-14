# TextAttachment

#### 项目介绍

```
- (void)viewDidLoad {
    [super viewDidLoad];
    NSTextAttachment *textAttachment = [[NSTextAttachment alloc] init];
    UIImage *image = [UIImage imageNamed:@"s.png"];
    textAttachment.image = image;
    textAttachment.bounds = CGRectMake(0, 0, image.size.width/image.scale, image.size.height/image.scale);
    
    NSMutableAttributedString *attri = [[NSMutableAttributedString alloc] initWithString:@"梅西去了伊比萨高端夜店lio Ibiza。结果在夜店中，梅西偶遇纳达尔。按照TyC电视台的说法，梅西和纳达尔进行了“简单但友好”的对话，并且进行了合影。尽管纳达尔是皇马死忠球迷，但他和梅西仍然惺惺相惜。" attributes:@{NSFontAttributeName:[UIFont systemFontOfSize:40]}];
    [attri appendAttributedString:[NSAttributedString attributedStringWithAttachment:textAttachment]];
    
    UILabel *label = [[UILabel alloc] initWithFrame:self.view.bounds];
    label.numberOfLines = 0;
    label.attributedText = attri;
    [self.view addSubview:label];
}
```
