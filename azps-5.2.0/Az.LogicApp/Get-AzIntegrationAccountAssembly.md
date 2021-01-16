---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountassembly
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountAssembly.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountAssembly.md
ms.openlocfilehash: 59b4ad9eb439808033233aa1677be16862c8a973
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98344569"
---
# <span data-ttu-id="91b60-101">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="91b60-101">Get-AzIntegrationAccountAssembly</span></span>

## <span data-ttu-id="91b60-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="91b60-102">SYNOPSIS</span></span>
<span data-ttu-id="91b60-103">Pobiera zestaw konta integracji.</span><span class="sxs-lookup"><span data-stu-id="91b60-103">Gets an integration account assembly.</span></span>

## <span data-ttu-id="91b60-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="91b60-104">SYNTAX</span></span>

### <span data-ttu-id="91b60-105">ByIntegrationAccount (domyślny)</span><span class="sxs-lookup"><span data-stu-id="91b60-105">ByIntegrationAccount (Default)</span></span>
```
Get-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="91b60-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="91b60-106">ByInputObject</span></span>
```
Get-AzIntegrationAccountAssembly -ParentObject <IntegrationAccount> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="91b60-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="91b60-107">ByResourceId</span></span>
```
Get-AzIntegrationAccountAssembly -ParentResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="91b60-108">Opis</span><span class="sxs-lookup"><span data-stu-id="91b60-108">DESCRIPTION</span></span>
<span data-ttu-id="91b60-109">Polecenie cmdlet **Get-AzIntegrationAccountAssembly** Pobiera zestaw z konta integracji.</span><span class="sxs-lookup"><span data-stu-id="91b60-109">The **Get-AzIntegrationAccountAssembly** cmdlet gets an assembly from an integration account.</span></span>

## <span data-ttu-id="91b60-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="91b60-110">EXAMPLES</span></span>

### <span data-ttu-id="91b60-111">Przykład 1: uzyskiwanie zestawu według parametrów</span><span class="sxs-lookup"><span data-stu-id="91b60-111">Example 1: Get an assembly by parameters</span></span>
```powershell
PS C:\> Get-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly"

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="91b60-112">Pobierz zestaw o nazwie "sampleAssembly" znajdujący się na koncie integracji "sampleIntegrationAccount", który jest zawarty w grupie zasobów "sampleResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="91b60-112">Get an assembly named "sampleAssembly" located in the integration account "sampleIntegrationAccount" which is contained in the resource group "sampleResourceGroup".</span></span>

### <span data-ttu-id="91b60-113">Przykład 2: wyświetlanie wszystkich zestawów w koncie integracji według parametrów</span><span class="sxs-lookup"><span data-stu-id="91b60-113">Example 2: List all assemblies in an integration account by parameters</span></span>
```powershell
PS C:\> Get-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount"

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly2
Name       : sampleAssembly2
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="91b60-114">Pobierz wszystkie zestawy zlokalizowane na koncie integracyjnym "sampleIntegrationAccount", które jest zawarte w grupie zasobów "sampleResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="91b60-114">Get all assemblies located in the integration account "sampleIntegrationAccount" which is contained in the resource group "sampleResourceGroup".</span></span>

## <span data-ttu-id="91b60-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="91b60-115">PARAMETERS</span></span>

### <span data-ttu-id="91b60-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91b60-116">-DefaultProfile</span></span>
<span data-ttu-id="91b60-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="91b60-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91b60-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="91b60-118">-Name</span></span>
<span data-ttu-id="91b60-119">Nazwa zestawu konta integracji.</span><span class="sxs-lookup"><span data-stu-id="91b60-119">The integration account assembly name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AssemblyName, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91b60-120">-Element nadrzędnyname</span><span class="sxs-lookup"><span data-stu-id="91b60-120">-ParentName</span></span>
<span data-ttu-id="91b60-121">Nazwa konta integracji.</span><span class="sxs-lookup"><span data-stu-id="91b60-121">The integration account name.</span></span>

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

### <span data-ttu-id="91b60-122">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="91b60-122">-ParentObject</span></span>
<span data-ttu-id="91b60-123">Obiekt konta integracji.</span><span class="sxs-lookup"><span data-stu-id="91b60-123">An integration account object.</span></span>

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

### <span data-ttu-id="91b60-124">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="91b60-124">-ParentResourceId</span></span>
<span data-ttu-id="91b60-125">Identyfikator zasobu konta integracji.</span><span class="sxs-lookup"><span data-stu-id="91b60-125">The integration account resource id.</span></span>

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

### <span data-ttu-id="91b60-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91b60-126">-ResourceGroupName</span></span>
<span data-ttu-id="91b60-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="91b60-127">The resource group name.</span></span>

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

### <span data-ttu-id="91b60-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91b60-128">CommonParameters</span></span>
<span data-ttu-id="91b60-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91b60-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91b60-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91b60-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91b60-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="91b60-131">INPUTS</span></span>

### <span data-ttu-id="91b60-132">Microsoft. Azure. Management. Logic. MODELES. IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="91b60-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

### <span data-ttu-id="91b60-133">System. String</span><span class="sxs-lookup"><span data-stu-id="91b60-133">System.String</span></span>

## <span data-ttu-id="91b60-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="91b60-134">OUTPUTS</span></span>

### <span data-ttu-id="91b60-135">Microsoft. Azure. Commands. LogicApp. models. PSIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="91b60-135">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

## <span data-ttu-id="91b60-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="91b60-136">NOTES</span></span>

## <span data-ttu-id="91b60-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="91b60-137">RELATED LINKS</span></span>
