---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountbatchconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountBatchConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountBatchConfiguration.md
ms.openlocfilehash: 26a2e414f05fc0aeb209afa946ae168c59ea4ff8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203745"
---
# <span data-ttu-id="3167c-101">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="3167c-101">Get-AzIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="3167c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3167c-102">SYNOPSIS</span></span>
<span data-ttu-id="3167c-103">Pobiera konfigurację partii konta integracji.</span><span class="sxs-lookup"><span data-stu-id="3167c-103">Gets an integration account batch configuration.</span></span>

## <span data-ttu-id="3167c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="3167c-104">SYNTAX</span></span>

### <span data-ttu-id="3167c-105">ByIntegrationAccount (domyślne)</span><span class="sxs-lookup"><span data-stu-id="3167c-105">ByIntegrationAccount (Default)</span></span>
```
Get-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3167c-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="3167c-106">ByInputObject</span></span>
```
Get-AzIntegrationAccountBatchConfiguration -ParentObject <IntegrationAccount> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3167c-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="3167c-107">ByResourceId</span></span>
```
Get-AzIntegrationAccountBatchConfiguration -ParentResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3167c-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="3167c-108">DESCRIPTION</span></span>
<span data-ttu-id="3167c-109">Polecenie **cmdlet Get-AzIntegrationAccountBatchConfiguration** pobiera konfigurację partii z konta integracji.</span><span class="sxs-lookup"><span data-stu-id="3167c-109">The **Get-AzIntegrationAccountBatchConfiguration** cmdlet gets an batch configuration from an integration account.</span></span>

## <span data-ttu-id="3167c-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="3167c-110">EXAMPLES</span></span>

### <span data-ttu-id="3167c-111">Przykład 1. Uzyskiwanie konfiguracji partii według parametrów</span><span class="sxs-lookup"><span data-stu-id="3167c-111">Example 1: Get a batch configuration by parameters</span></span>
```powershell
PS C:\> Get-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig"

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="3167c-112">Pobierz konfigurację partii o nazwie "sampleBatchConfig" znajdującą się na koncie integracji "sampleIntegrationAccount", które znajduje się w grupie zasobów "sampleResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="3167c-112">Get a batch configuration named "sampleBatchConfig" located in the integration account "sampleIntegrationAccount" which is contained in the resource group "sampleResourceGroup".</span></span>

### <span data-ttu-id="3167c-113">Przykład 2. Lista wszystkich konfiguracji wsadowych na koncie integracji według parametrów</span><span class="sxs-lookup"><span data-stu-id="3167c-113">Example 2: List all batch configurations in an integration account by parameters</span></span>
```powershell
PS C:\> Get-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount"

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig2
Name       : sampleBatchConfig2
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="3167c-114">Uzyskaj wszystkie konfiguracje partii znajdujące się na koncie integracji "sampleIntegrationAccount", które jest zawarte w grupie zasobów "sampleResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="3167c-114">Get all batch configurations located in the integration account "sampleIntegrationAccount" which is contained in the resource group "sampleResourceGroup".</span></span>

## <span data-ttu-id="3167c-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3167c-115">PARAMETERS</span></span>

### <span data-ttu-id="3167c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3167c-116">-DefaultProfile</span></span>
<span data-ttu-id="3167c-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="3167c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3167c-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="3167c-118">-Name</span></span>
<span data-ttu-id="3167c-119">Nazwa partii partii konta integracji.</span><span class="sxs-lookup"><span data-stu-id="3167c-119">The integration account batch configuration name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BatchConfigurationName, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3167c-120">-ParentName</span><span class="sxs-lookup"><span data-stu-id="3167c-120">-ParentName</span></span>
<span data-ttu-id="3167c-121">Nazwa konta integracji.</span><span class="sxs-lookup"><span data-stu-id="3167c-121">The integration account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccount
Aliases: IntegrationAccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3167c-122">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="3167c-122">-ParentObject</span></span>
<span data-ttu-id="3167c-123">Obiekt konta integracji.</span><span class="sxs-lookup"><span data-stu-id="3167c-123">An integration account object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Logic.Models.IntegrationAccount
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3167c-124">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="3167c-124">-ParentResourceId</span></span>
<span data-ttu-id="3167c-125">Identyfikator zasobu konta integracji.</span><span class="sxs-lookup"><span data-stu-id="3167c-125">The integration account resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3167c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3167c-126">-ResourceGroupName</span></span>
<span data-ttu-id="3167c-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3167c-127">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccount
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3167c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3167c-128">CommonParameters</span></span>
<span data-ttu-id="3167c-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3167c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3167c-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3167c-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3167c-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3167c-131">INPUTS</span></span>

### <span data-ttu-id="3167c-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="3167c-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

### <span data-ttu-id="3167c-133">System.String</span><span class="sxs-lookup"><span data-stu-id="3167c-133">System.String</span></span>

## <span data-ttu-id="3167c-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3167c-134">OUTPUTS</span></span>

### <span data-ttu-id="3167c-135">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="3167c-135">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="3167c-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="3167c-136">NOTES</span></span>

## <span data-ttu-id="3167c-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3167c-137">RELATED LINKS</span></span>
