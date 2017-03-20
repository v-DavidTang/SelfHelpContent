 <properties
    pageTitle="Business to Consumer (B2C)/Session token configuration not being enforced"
    description="企业对消费者 (B2C)/未强制实施会话令牌配置"
    service="microsoft.azureactivedirectory"
    resource="b2cDirectories"
    authors="parakhj"
    displayOrder="5"
    selfHelpType="resource"
    supportTopicIds="32416703"
    resourceTags=""
    productPesIds=""
    cloudEnvironments="public"
/>


# <a name="session-token-configuration-is-not-being-enforced"></a>未强制实施会话令牌配置

如果使用“登录”策略，则不会强制使用你的自定义会话令牌持续时间。 解决方法是改用组合的“登录/注册”策略。 此问题源于以下事实：“注册或登录”策略利用了与旧版“登录”策略相比而言更新或已改进的策略实施。
