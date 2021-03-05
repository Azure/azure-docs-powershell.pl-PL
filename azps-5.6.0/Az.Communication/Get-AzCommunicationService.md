---
external help file: ''
Module Name: Az.Communication
online version: https://docs.microsoft.com/powershell/module/az.communication/get-azcommunicationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Get-AzCommunicationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Get-AzCommunicationService.md
ms.openlocfilehash: f9f4cc86a07c50718511c3ed0889d96f7acec9a7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991670"
---
# <span data-ttu-id="c55eb-101">Get-AzCommunicationService</span><span class="sxs-lookup"><span data-stu-id="c55eb-101">Get-AzCommunicationService</span></span>

## <span data-ttu-id="c55eb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c55eb-102">SYNOPSIS</span></span>
<span data-ttu-id="c55eb-103">Uzyskaj usługę CommunicationService i jej właściwości.</span><span class="sxs-lookup"><span data-stu-id="c55eb-103">Get the CommunicationService and its properties.</span></span>

## <span data-ttu-id="c55eb-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c55eb-104">SYNTAX</span></span>

### <span data-ttu-id="c55eb-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="c55eb-105">List (Default)</span></span>
```
Get-AzCommunicationService [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c55eb-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="c55eb-106">Get</span></span>
```
Get-AzCommunicationService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c55eb-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c55eb-107">GetViaIdentity</span></span>
```
Get-AzCommunicationService -InputObject <ICommunicationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="c55eb-108">Lista1</span><span class="sxs-lookup"><span data-stu-id="c55eb-108">List1</span></span>
```
Get-AzCommunicationService -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="c55eb-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="c55eb-109">DESCRIPTION</span></span>
<span data-ttu-id="c55eb-110">Uzyskaj usługę CommunicationService i jej właściwości.</span><span class="sxs-lookup"><span data-stu-id="c55eb-110">Get the CommunicationService and its properties.</span></span>

## <span data-ttu-id="c55eb-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c55eb-111">EXAMPLES</span></span>

### <span data-ttu-id="c55eb-112">Przykład 1. Lista istniejących usług communicationservices dla subskrypcji</span><span class="sxs-lookup"><span data-stu-id="c55eb-112">Example 1: List existing CommunicationServices for a Subscription</span></span>
```powershell
PS C:\> Get-AzCommunicationService -SubscriptionId 73fc3592-3cef-4300-5e19-8d18b65ce0e8

Location Name             Type                                          AzureAsyncOperation
-------- ----             ----                                          -------------------
global   ContosoResource1   Microsoft.Communication/communicationServices
global   ContosoResource4   Microsoft.Communication/communicationServices
global   ContosoResource3   Microsoft.Communication/communicationServices
global   ContosoResource5   Microsoft.Communication/communicationServices
```

<span data-ttu-id="c55eb-113">Zwraca listę wszystkich zasobów ACS w ramach tej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="c55eb-113">Returns a list of all ACS resources under that subscription.</span></span>

### <span data-ttu-id="c55eb-114">Przykład 2. Uzyskiwanie informacji o określonym zasobie Azure Communication</span><span class="sxs-lookup"><span data-stu-id="c55eb-114">Example 2: Get infomation on specified Azure Communication resource</span></span>
```powershell
PS C:\> Get-AzCommunicationService -Name ContosoAcsResource1 -ResourceGroupName ContosoResourceProvider1

Location Name           Type                                          AzureAsyncOperation
-------- ----           ----                                          -------------------
Global   ContosoAcsResource1 Microsoft.Communication/communicationServices
```

<span data-ttu-id="c55eb-115">Zwraca informacje dotyczące zasobu ACS, jeśli zostanie znaleziony jeden zgodny z dostarczonymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="c55eb-115">Returns the information on an ACS resource, if one matching provided parameters is found.</span></span>

## <span data-ttu-id="c55eb-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c55eb-116">PARAMETERS</span></span>

### <span data-ttu-id="c55eb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c55eb-117">-DefaultProfile</span></span>
<span data-ttu-id="c55eb-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c55eb-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c55eb-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c55eb-119">-InputObject</span></span>
<span data-ttu-id="c55eb-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="c55eb-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c55eb-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="c55eb-121">-Name</span></span>
<span data-ttu-id="c55eb-122">Nazwa zasobu CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="c55eb-122">The name of the CommunicationService resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: CommunicationServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c55eb-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c55eb-123">-ResourceGroupName</span></span>
<span data-ttu-id="c55eb-124">Nazwa grupy zasobów zawierającej zasób.</span><span class="sxs-lookup"><span data-stu-id="c55eb-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="c55eb-125">Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.</span><span class="sxs-lookup"><span data-stu-id="c55eb-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c55eb-126">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c55eb-126">-SubscriptionId</span></span>
<span data-ttu-id="c55eb-127">Pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="c55eb-127">Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="c55eb-128">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="c55eb-128">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c55eb-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c55eb-129">CommonParameters</span></span>
<span data-ttu-id="c55eb-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c55eb-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c55eb-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c55eb-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c55eb-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c55eb-132">INPUTS</span></span>

### <span data-ttu-id="c55eb-133">Microsoft.Azure.PowerShell.cmdlet.Communication.Models.ICommunicationIdentity</span><span class="sxs-lookup"><span data-stu-id="c55eb-133">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity</span></span>

## <span data-ttu-id="c55eb-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c55eb-134">OUTPUTS</span></span>

### <span data-ttu-id="c55eb-135">Microsoft.Azure.PowerShell.cmdlet.Communication.Models.Api200820Preview.ICommunicationServiceResource</span><span class="sxs-lookup"><span data-stu-id="c55eb-135">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceResource</span></span>

## <span data-ttu-id="c55eb-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c55eb-136">NOTES</span></span>

<span data-ttu-id="c55eb-137">ALIASY</span><span class="sxs-lookup"><span data-stu-id="c55eb-137">ALIASES</span></span>

<span data-ttu-id="c55eb-138">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c55eb-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c55eb-139">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="c55eb-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c55eb-140">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c55eb-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c55eb-141">INPUTOBJECT: <ICommunicationIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="c55eb-141">INPUTOBJECT <ICommunicationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c55eb-142">`[CommunicationServiceName <String>]`: nazwa zasobu CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="c55eb-142">`[CommunicationServiceName <String>]`: The name of the CommunicationService resource.</span></span>
  - <span data-ttu-id="c55eb-143">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="c55eb-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c55eb-144">`[Location <String>]`: Region platformy Azure</span><span class="sxs-lookup"><span data-stu-id="c55eb-144">`[Location <String>]`: The Azure region</span></span>
  - <span data-ttu-id="c55eb-145">`[OperationId <String>]`: Identyfikator trwającej operacji synchronizacji</span><span class="sxs-lookup"><span data-stu-id="c55eb-145">`[OperationId <String>]`: The ID of an ongoing async operation</span></span>
  - <span data-ttu-id="c55eb-146">`[ResourceGroupName <String>]`: nazwa grupy zasobów, która zawiera zasób.</span><span class="sxs-lookup"><span data-stu-id="c55eb-146">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="c55eb-147">Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.</span><span class="sxs-lookup"><span data-stu-id="c55eb-147">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="c55eb-148">`[SubscriptionId <String>]`: Otrzymuje identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="c55eb-148">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="c55eb-149">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="c55eb-149">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="c55eb-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c55eb-150">RELATED LINKS</span></span>

