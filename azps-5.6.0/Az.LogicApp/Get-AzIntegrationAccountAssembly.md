---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/powershell/module/az.logicapp/get-azintegrationaccountassembly
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountAssembly.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountAssembly.md
ms.openlocfilehash: 95daa8025dde470e85d0e00e09c00f26d08e1342
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007802"
---
# <span data-ttu-id="9b11f-101">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="9b11f-101">Get-AzIntegrationAccountAssembly</span></span>

## <span data-ttu-id="9b11f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b11f-102">SYNOPSIS</span></span>
<span data-ttu-id="9b11f-103">Otrzymuje zestaw konta integracji.</span><span class="sxs-lookup"><span data-stu-id="9b11f-103">Gets an integration account assembly.</span></span>

## <span data-ttu-id="9b11f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9b11f-104">SYNTAX</span></span>

### <span data-ttu-id="9b11f-105">ByIntegrationAccount (domyślne)</span><span class="sxs-lookup"><span data-stu-id="9b11f-105">ByIntegrationAccount (Default)</span></span>
```
Get-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b11f-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="9b11f-106">ByInputObject</span></span>
```
Get-AzIntegrationAccountAssembly -ParentObject <IntegrationAccount> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b11f-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="9b11f-107">ByResourceId</span></span>
```
Get-AzIntegrationAccountAssembly -ParentResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9b11f-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="9b11f-108">DESCRIPTION</span></span>
<span data-ttu-id="9b11f-109">Polecenie **cmdlet Get-AzIntegrationAccountAssembly** pobiera zestaw z konta integracji.</span><span class="sxs-lookup"><span data-stu-id="9b11f-109">The **Get-AzIntegrationAccountAssembly** cmdlet gets an assembly from an integration account.</span></span>

## <span data-ttu-id="9b11f-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9b11f-110">EXAMPLES</span></span>

### <span data-ttu-id="9b11f-111">Przykład 1. Uzyskiwanie zestawu według parametrów</span><span class="sxs-lookup"><span data-stu-id="9b11f-111">Example 1: Get an assembly by parameters</span></span>
```powershell
PS C:\> Get-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly"

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="9b11f-112">Uzyskaj zestaw o nazwie "sampleAssembly" znajdujący się na koncie integracji "sampleIntegrationAccount", które znajduje się w grupie zasobów "sampleResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="9b11f-112">Get an assembly named "sampleAssembly" located in the integration account "sampleIntegrationAccount" which is contained in the resource group "sampleResourceGroup".</span></span>

### <span data-ttu-id="9b11f-113">Przykład 2. Lista wszystkich zestawów na koncie integracji według parametrów</span><span class="sxs-lookup"><span data-stu-id="9b11f-113">Example 2: List all assemblies in an integration account by parameters</span></span>
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

<span data-ttu-id="9b11f-114">Pobierz wszystkie zestawy znajdujące się na koncie integracji "sampleIntegrationAccount", które znajduje się w grupie zasobów "sampleResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="9b11f-114">Get all assemblies located in the integration account "sampleIntegrationAccount" which is contained in the resource group "sampleResourceGroup".</span></span>

## <span data-ttu-id="9b11f-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9b11f-115">PARAMETERS</span></span>

### <span data-ttu-id="9b11f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b11f-116">-DefaultProfile</span></span>
<span data-ttu-id="9b11f-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9b11f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b11f-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="9b11f-118">-Name</span></span>
<span data-ttu-id="9b11f-119">Nazwa zestawu konta integracji.</span><span class="sxs-lookup"><span data-stu-id="9b11f-119">The integration account assembly name.</span></span>

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

### <span data-ttu-id="9b11f-120">-ParentName</span><span class="sxs-lookup"><span data-stu-id="9b11f-120">-ParentName</span></span>
<span data-ttu-id="9b11f-121">Nazwa konta integracji.</span><span class="sxs-lookup"><span data-stu-id="9b11f-121">The integration account name.</span></span>

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

### <span data-ttu-id="9b11f-122">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="9b11f-122">-ParentObject</span></span>
<span data-ttu-id="9b11f-123">Obiekt konta integracji.</span><span class="sxs-lookup"><span data-stu-id="9b11f-123">An integration account object.</span></span>

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

### <span data-ttu-id="9b11f-124">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="9b11f-124">-ParentResourceId</span></span>
<span data-ttu-id="9b11f-125">Identyfikator zasobu konta integracji.</span><span class="sxs-lookup"><span data-stu-id="9b11f-125">The integration account resource id.</span></span>

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

### <span data-ttu-id="9b11f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b11f-126">-ResourceGroupName</span></span>
<span data-ttu-id="9b11f-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9b11f-127">The resource group name.</span></span>

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

### <span data-ttu-id="9b11f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b11f-128">CommonParameters</span></span>
<span data-ttu-id="9b11f-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b11f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b11f-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b11f-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b11f-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9b11f-131">INPUTS</span></span>

### <span data-ttu-id="9b11f-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="9b11f-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

### <span data-ttu-id="9b11f-133">System.String</span><span class="sxs-lookup"><span data-stu-id="9b11f-133">System.String</span></span>

## <span data-ttu-id="9b11f-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9b11f-134">OUTPUTS</span></span>

### <span data-ttu-id="9b11f-135">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="9b11f-135">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

## <span data-ttu-id="9b11f-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9b11f-136">NOTES</span></span>

## <span data-ttu-id="9b11f-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9b11f-137">RELATED LINKS</span></span>
