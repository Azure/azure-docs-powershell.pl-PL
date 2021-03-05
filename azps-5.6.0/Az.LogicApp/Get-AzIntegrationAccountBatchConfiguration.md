---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/powershell/module/az.logicapp/get-azintegrationaccountbatchconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountBatchConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountBatchConfiguration.md
ms.openlocfilehash: 722f2bd79230de11c12ab0448fb39ed3ad49f00d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960705"
---
# <span data-ttu-id="8ee92-101">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="8ee92-101">Get-AzIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="8ee92-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ee92-102">SYNOPSIS</span></span>
<span data-ttu-id="8ee92-103">Pobiera konfigurację partii konta integracji.</span><span class="sxs-lookup"><span data-stu-id="8ee92-103">Gets an integration account batch configuration.</span></span>

## <span data-ttu-id="8ee92-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8ee92-104">SYNTAX</span></span>

### <span data-ttu-id="8ee92-105">ByIntegrationAccount (domyślne)</span><span class="sxs-lookup"><span data-stu-id="8ee92-105">ByIntegrationAccount (Default)</span></span>
```
Get-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8ee92-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="8ee92-106">ByInputObject</span></span>
```
Get-AzIntegrationAccountBatchConfiguration -ParentObject <IntegrationAccount> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8ee92-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8ee92-107">ByResourceId</span></span>
```
Get-AzIntegrationAccountBatchConfiguration -ParentResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8ee92-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="8ee92-108">DESCRIPTION</span></span>
<span data-ttu-id="8ee92-109">Polecenie **cmdlet Get-AzIntegrationAccountBatchConfiguration** pobiera konfigurację partii z konta integracji.</span><span class="sxs-lookup"><span data-stu-id="8ee92-109">The **Get-AzIntegrationAccountBatchConfiguration** cmdlet gets an batch configuration from an integration account.</span></span>

## <span data-ttu-id="8ee92-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8ee92-110">EXAMPLES</span></span>

### <span data-ttu-id="8ee92-111">Przykład 1. Uzyskiwanie konfiguracji partii według parametrów</span><span class="sxs-lookup"><span data-stu-id="8ee92-111">Example 1: Get a batch configuration by parameters</span></span>
```powershell
PS C:\> Get-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig"

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="8ee92-112">Pobierz konfigurację partii o nazwie "sampleBatchConfig" znajdującą się na koncie integracji "sampleIntegrationAccount", które znajduje się w grupie zasobów "sampleResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="8ee92-112">Get a batch configuration named "sampleBatchConfig" located in the integration account "sampleIntegrationAccount" which is contained in the resource group "sampleResourceGroup".</span></span>

### <span data-ttu-id="8ee92-113">Przykład 2. Lista wszystkich konfiguracji wsadowych na koncie integracji według parametrów</span><span class="sxs-lookup"><span data-stu-id="8ee92-113">Example 2: List all batch configurations in an integration account by parameters</span></span>
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

<span data-ttu-id="8ee92-114">Uzyskaj wszystkie konfiguracje partii znajdujące się na koncie integracji "sampleIntegrationAccount", które jest zawarte w grupie zasobów "sampleResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="8ee92-114">Get all batch configurations located in the integration account "sampleIntegrationAccount" which is contained in the resource group "sampleResourceGroup".</span></span>

## <span data-ttu-id="8ee92-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8ee92-115">PARAMETERS</span></span>

### <span data-ttu-id="8ee92-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ee92-116">-DefaultProfile</span></span>
<span data-ttu-id="8ee92-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8ee92-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ee92-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="8ee92-118">-Name</span></span>
<span data-ttu-id="8ee92-119">Nazwa partii partii konta integracji.</span><span class="sxs-lookup"><span data-stu-id="8ee92-119">The integration account batch configuration name.</span></span>

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

### <span data-ttu-id="8ee92-120">-ParentName</span><span class="sxs-lookup"><span data-stu-id="8ee92-120">-ParentName</span></span>
<span data-ttu-id="8ee92-121">Nazwa konta integracji.</span><span class="sxs-lookup"><span data-stu-id="8ee92-121">The integration account name.</span></span>

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

### <span data-ttu-id="8ee92-122">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="8ee92-122">-ParentObject</span></span>
<span data-ttu-id="8ee92-123">Obiekt konta integracji.</span><span class="sxs-lookup"><span data-stu-id="8ee92-123">An integration account object.</span></span>

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

### <span data-ttu-id="8ee92-124">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="8ee92-124">-ParentResourceId</span></span>
<span data-ttu-id="8ee92-125">Identyfikator zasobu konta integracji.</span><span class="sxs-lookup"><span data-stu-id="8ee92-125">The integration account resource id.</span></span>

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

### <span data-ttu-id="8ee92-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ee92-126">-ResourceGroupName</span></span>
<span data-ttu-id="8ee92-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8ee92-127">The resource group name.</span></span>

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

### <span data-ttu-id="8ee92-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ee92-128">CommonParameters</span></span>
<span data-ttu-id="8ee92-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ee92-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ee92-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ee92-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ee92-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8ee92-131">INPUTS</span></span>

### <span data-ttu-id="8ee92-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="8ee92-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

### <span data-ttu-id="8ee92-133">System.String</span><span class="sxs-lookup"><span data-stu-id="8ee92-133">System.String</span></span>

## <span data-ttu-id="8ee92-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8ee92-134">OUTPUTS</span></span>

### <span data-ttu-id="8ee92-135">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="8ee92-135">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="8ee92-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8ee92-136">NOTES</span></span>

## <span data-ttu-id="8ee92-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8ee92-137">RELATED LINKS</span></span>
