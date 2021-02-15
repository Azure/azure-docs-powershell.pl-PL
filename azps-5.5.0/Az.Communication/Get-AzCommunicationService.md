---
external help file: ''
Module Name: Az.Communication
online version: https://docs.microsoft.com/en-us/powershell/module/az.communication/get-azcommunicationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Get-AzCommunicationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Get-AzCommunicationService.md
ms.openlocfilehash: 3101ca2b120860dfa6df95786e235fc88fd0fc78
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200691"
---
# <span data-ttu-id="2fced-101">Get-AzCommunicationService</span><span class="sxs-lookup"><span data-stu-id="2fced-101">Get-AzCommunicationService</span></span>

## <span data-ttu-id="2fced-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2fced-102">SYNOPSIS</span></span>
<span data-ttu-id="2fced-103">Uzyskaj usługę CommunicationService i jej właściwości.</span><span class="sxs-lookup"><span data-stu-id="2fced-103">Get the CommunicationService and its properties.</span></span>

## <span data-ttu-id="2fced-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2fced-104">SYNTAX</span></span>

### <span data-ttu-id="2fced-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="2fced-105">List (Default)</span></span>
```
Get-AzCommunicationService [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="2fced-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="2fced-106">Get</span></span>
```
Get-AzCommunicationService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="2fced-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="2fced-107">GetViaIdentity</span></span>
```
Get-AzCommunicationService -InputObject <ICommunicationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="2fced-108">Lista1</span><span class="sxs-lookup"><span data-stu-id="2fced-108">List1</span></span>
```
Get-AzCommunicationService -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="2fced-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="2fced-109">DESCRIPTION</span></span>
<span data-ttu-id="2fced-110">Uzyskaj usługę CommunicationService i jej właściwości.</span><span class="sxs-lookup"><span data-stu-id="2fced-110">Get the CommunicationService and its properties.</span></span>

## <span data-ttu-id="2fced-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2fced-111">EXAMPLES</span></span>

### <span data-ttu-id="2fced-112">Przykład 1. Lista istniejących usług communicationservices dla subskrypcji</span><span class="sxs-lookup"><span data-stu-id="2fced-112">Example 1: List existing CommunicationServices for a Subscription</span></span>
```powershell
PS C:\> Get-AzCommunicationService -SubscriptionId 73fc3592-3cef-4300-5e19-8d18b65ce0e8

Location Name             Type                                          AzureAsyncOperation
-------- ----             ----                                          -------------------
global   ContosoResource1   Microsoft.Communication/communicationServices
global   ContosoResource4   Microsoft.Communication/communicationServices
global   ContosoResource3   Microsoft.Communication/communicationServices
global   ContosoResource5   Microsoft.Communication/communicationServices
```

<span data-ttu-id="2fced-113">Zwraca listę wszystkich zasobów ACS w ramach tej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="2fced-113">Returns a list of all ACS resources under that subscription.</span></span>

### <span data-ttu-id="2fced-114">Przykład 2. Uzyskiwanie informacji o określonym zasobie Azure Communication</span><span class="sxs-lookup"><span data-stu-id="2fced-114">Example 2: Get infomation on specified Azure Communication resource</span></span>
```powershell
PS C:\> Get-AzCommunicationService -Name ContosoAcsResource1 -ResourceGroupName ContosoResourceProvider1

Location Name           Type                                          AzureAsyncOperation
-------- ----           ----                                          -------------------
Global   ContosoAcsResource1 Microsoft.Communication/communicationServices
```

<span data-ttu-id="2fced-115">Zwraca informacje dotyczące zasobu ACS, jeśli zostanie znaleziony jeden zgodny z dostarczonymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="2fced-115">Returns the information on an ACS resource, if one matching provided parameters is found.</span></span>

## <span data-ttu-id="2fced-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2fced-116">PARAMETERS</span></span>

### <span data-ttu-id="2fced-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fced-117">-DefaultProfile</span></span>
<span data-ttu-id="2fced-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="2fced-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2fced-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2fced-119">-InputObject</span></span>
<span data-ttu-id="2fced-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="2fced-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="2fced-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="2fced-121">-Name</span></span>
<span data-ttu-id="2fced-122">Nazwa zasobu CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="2fced-122">The name of the CommunicationService resource.</span></span>

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

### <span data-ttu-id="2fced-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2fced-123">-ResourceGroupName</span></span>
<span data-ttu-id="2fced-124">Nazwa grupy zasobów, która zawiera zasób.</span><span class="sxs-lookup"><span data-stu-id="2fced-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="2fced-125">Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.</span><span class="sxs-lookup"><span data-stu-id="2fced-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="2fced-126">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2fced-126">-SubscriptionId</span></span>
<span data-ttu-id="2fced-127">Pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="2fced-127">Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="2fced-128">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="2fced-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="2fced-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fced-129">CommonParameters</span></span>
<span data-ttu-id="2fced-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2fced-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fced-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2fced-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fced-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2fced-132">INPUTS</span></span>

### <span data-ttu-id="2fced-133">Microsoft.Azure.PowerShell.Cmdlet.Communication.Models.ICommunicationIdentity</span><span class="sxs-lookup"><span data-stu-id="2fced-133">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity</span></span>

## <span data-ttu-id="2fced-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2fced-134">OUTPUTS</span></span>

### <span data-ttu-id="2fced-135">Microsoft.Azure.PowerShell.cmdlet.Communication.Models.Api20200820Preview.ICommunicationServiceResource</span><span class="sxs-lookup"><span data-stu-id="2fced-135">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceResource</span></span>

## <span data-ttu-id="2fced-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2fced-136">NOTES</span></span>

<span data-ttu-id="2fced-137">ALIASY</span><span class="sxs-lookup"><span data-stu-id="2fced-137">ALIASES</span></span>

<span data-ttu-id="2fced-138">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="2fced-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2fced-139">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótu zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="2fced-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2fced-140">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2fced-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2fced-141">INPUTOBJECT: <ICommunicationIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="2fced-141">INPUTOBJECT <ICommunicationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2fced-142">`[CommunicationServiceName <String>]`: nazwa zasobu CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="2fced-142">`[CommunicationServiceName <String>]`: The name of the CommunicationService resource.</span></span>
  - <span data-ttu-id="2fced-143">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="2fced-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2fced-144">`[Location <String>]`: Region platformy Azure</span><span class="sxs-lookup"><span data-stu-id="2fced-144">`[Location <String>]`: The Azure region</span></span>
  - <span data-ttu-id="2fced-145">`[OperationId <String>]`: Identyfikator trwającej operacji synchronizacji</span><span class="sxs-lookup"><span data-stu-id="2fced-145">`[OperationId <String>]`: The ID of an ongoing async operation</span></span>
  - <span data-ttu-id="2fced-146">`[ResourceGroupName <String>]`: nazwa grupy zasobów, która zawiera zasób.</span><span class="sxs-lookup"><span data-stu-id="2fced-146">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="2fced-147">Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.</span><span class="sxs-lookup"><span data-stu-id="2fced-147">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="2fced-148">`[SubscriptionId <String>]`: Otrzymuje identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="2fced-148">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="2fced-149">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="2fced-149">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="2fced-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2fced-150">RELATED LINKS</span></span>

