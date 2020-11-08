---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountbatchconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountBatchConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountBatchConfiguration.md
ms.openlocfilehash: 26a2e414f05fc0aeb209afa946ae168c59ea4ff8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94220803"
---
# <span data-ttu-id="2acd0-101">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="2acd0-101">Get-AzIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="2acd0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2acd0-102">SYNOPSIS</span></span>
<span data-ttu-id="2acd0-103">Pobiera konfigurację partii konta integracji.</span><span class="sxs-lookup"><span data-stu-id="2acd0-103">Gets an integration account batch configuration.</span></span>

## <span data-ttu-id="2acd0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2acd0-104">SYNTAX</span></span>

### <span data-ttu-id="2acd0-105">ByIntegrationAccount (domyślny)</span><span class="sxs-lookup"><span data-stu-id="2acd0-105">ByIntegrationAccount (Default)</span></span>
```
Get-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2acd0-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="2acd0-106">ByInputObject</span></span>
```
Get-AzIntegrationAccountBatchConfiguration -ParentObject <IntegrationAccount> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2acd0-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="2acd0-107">ByResourceId</span></span>
```
Get-AzIntegrationAccountBatchConfiguration -ParentResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2acd0-108">Opis</span><span class="sxs-lookup"><span data-stu-id="2acd0-108">DESCRIPTION</span></span>
<span data-ttu-id="2acd0-109">Polecenie cmdlet **Get-AzIntegrationAccountBatchConfiguration** Pobiera konfigurację partii z konta integracji.</span><span class="sxs-lookup"><span data-stu-id="2acd0-109">The **Get-AzIntegrationAccountBatchConfiguration** cmdlet gets an batch configuration from an integration account.</span></span>

## <span data-ttu-id="2acd0-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2acd0-110">EXAMPLES</span></span>

### <span data-ttu-id="2acd0-111">Przykład 1: Uzyskiwanie konfiguracji wsadowej według parametrów</span><span class="sxs-lookup"><span data-stu-id="2acd0-111">Example 1: Get a batch configuration by parameters</span></span>
```powershell
PS C:\> Get-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig"

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="2acd0-112">Pobierz konfigurację wsadową o nazwie "sampleBatchConfig" znajdującą się na koncie integracyjnym "sampleIntegrationAccount", który jest zawarty w grupie zasobów "sampleResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="2acd0-112">Get a batch configuration named "sampleBatchConfig" located in the integration account "sampleIntegrationAccount" which is contained in the resource group "sampleResourceGroup".</span></span>

### <span data-ttu-id="2acd0-113">Przykład 2: wyświetlanie wszystkich konfiguracji partii w ramach konta integracji według parametrów</span><span class="sxs-lookup"><span data-stu-id="2acd0-113">Example 2: List all batch configurations in an integration account by parameters</span></span>
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

<span data-ttu-id="2acd0-114">Pobierz wszystkie konfiguracje wsadowe zlokalizowane na koncie integracyjnym "sampleIntegrationAccount", które jest zawarte w grupie zasobów "sampleResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="2acd0-114">Get all batch configurations located in the integration account "sampleIntegrationAccount" which is contained in the resource group "sampleResourceGroup".</span></span>

## <span data-ttu-id="2acd0-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2acd0-115">PARAMETERS</span></span>

### <span data-ttu-id="2acd0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2acd0-116">-DefaultProfile</span></span>
<span data-ttu-id="2acd0-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2acd0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2acd0-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2acd0-118">-Name</span></span>
<span data-ttu-id="2acd0-119">Nazwa konfiguracji wsadowej konta integracji.</span><span class="sxs-lookup"><span data-stu-id="2acd0-119">The integration account batch configuration name.</span></span>

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

### <span data-ttu-id="2acd0-120">-Element nadrzędnyname</span><span class="sxs-lookup"><span data-stu-id="2acd0-120">-ParentName</span></span>
<span data-ttu-id="2acd0-121">Nazwa konta integracji.</span><span class="sxs-lookup"><span data-stu-id="2acd0-121">The integration account name.</span></span>

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

### <span data-ttu-id="2acd0-122">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="2acd0-122">-ParentObject</span></span>
<span data-ttu-id="2acd0-123">Obiekt konta integracji.</span><span class="sxs-lookup"><span data-stu-id="2acd0-123">An integration account object.</span></span>

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

### <span data-ttu-id="2acd0-124">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="2acd0-124">-ParentResourceId</span></span>
<span data-ttu-id="2acd0-125">Identyfikator zasobu konta integracji.</span><span class="sxs-lookup"><span data-stu-id="2acd0-125">The integration account resource id.</span></span>

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

### <span data-ttu-id="2acd0-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2acd0-126">-ResourceGroupName</span></span>
<span data-ttu-id="2acd0-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2acd0-127">The resource group name.</span></span>

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

### <span data-ttu-id="2acd0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2acd0-128">CommonParameters</span></span>
<span data-ttu-id="2acd0-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2acd0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2acd0-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2acd0-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2acd0-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2acd0-131">INPUTS</span></span>

### <span data-ttu-id="2acd0-132">Microsoft. Azure. Management. Logic. MODELES. IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="2acd0-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

### <span data-ttu-id="2acd0-133">System. String</span><span class="sxs-lookup"><span data-stu-id="2acd0-133">System.String</span></span>

## <span data-ttu-id="2acd0-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2acd0-134">OUTPUTS</span></span>

### <span data-ttu-id="2acd0-135">Microsoft. Azure. Commands. LogicApp. models. PSIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="2acd0-135">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="2acd0-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2acd0-136">NOTES</span></span>

## <span data-ttu-id="2acd0-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2acd0-137">RELATED LINKS</span></span>
