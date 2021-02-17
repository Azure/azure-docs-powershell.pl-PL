---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.digitaltwins/get-azdigitaltwinsendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Get-AzDigitalTwinsEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Get-AzDigitalTwinsEndpoint.md
ms.openlocfilehash: 6299fcc8828031b61aabc912fcd30c1ed8cbb0e2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188514"
---
# <span data-ttu-id="41cfc-101">Get-AzDigitalTwinsEndpoint</span><span class="sxs-lookup"><span data-stu-id="41cfc-101">Get-AzDigitalTwinsEndpoint</span></span>

## <span data-ttu-id="41cfc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41cfc-102">SYNOPSIS</span></span>
<span data-ttu-id="41cfc-103">Uzyskaj punkt końcowy DigitalTwinsInstances.</span><span class="sxs-lookup"><span data-stu-id="41cfc-103">Get DigitalTwinsInstances Endpoint.</span></span>

## <span data-ttu-id="41cfc-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="41cfc-104">SYNTAX</span></span>

### <span data-ttu-id="41cfc-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="41cfc-105">List (Default)</span></span>
```
Get-AzDigitalTwinsEndpoint -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="41cfc-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="41cfc-106">Get</span></span>
```
Get-AzDigitalTwinsEndpoint -EndpointName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="41cfc-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="41cfc-107">GetViaIdentity</span></span>
```
Get-AzDigitalTwinsEndpoint -InputObject <IDigitalTwinsIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="41cfc-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="41cfc-108">DESCRIPTION</span></span>
<span data-ttu-id="41cfc-109">Uzyskaj punkt końcowy DigitalTwinsInstances.</span><span class="sxs-lookup"><span data-stu-id="41cfc-109">Get DigitalTwinsInstances Endpoint.</span></span>

## <span data-ttu-id="41cfc-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="41cfc-110">EXAMPLES</span></span>

### <span data-ttu-id="41cfc-111">Przykład 1. Lista azDigitalTwinsEndpoint w grupie Zasobów</span><span class="sxs-lookup"><span data-stu-id="41cfc-111">Example 1: List AzDigitalTwinsEndpoint in ResourceGroup</span></span>
```powershell
PS C:\> Get-AzDigitalTwinsEndpoint -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest

Name                     Type
----                     ----
youriDigitalTwinEndpoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="41cfc-112">Lista wszystkich elementów AzDigitalTwinsEndpoints według nazwy ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41cfc-112">List all AzDigitalTwinsEndpoints by ResourceGroupName</span></span>

### <span data-ttu-id="41cfc-113">Przykład 2. Pobierz plik AzDigitalTwinsEndpoint według wartości EndpointName</span><span class="sxs-lookup"><span data-stu-id="41cfc-113">Example 2: Get AzDigitalTwinsEndpoint by EndpointName</span></span>
```powershell
PS C:\> Get-AzDigitalTwinsEndpoint -EndpointName youriDigitalTwinEndpoint -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest

Name                     Type
----                     ----
youriDigitalTwinEndpoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="41cfc-114">Uzyskiwanie pliku AzDigitalTwinsEndpoint według nazwy endpoint w grupie ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="41cfc-114">Get AzDigitalTwinsEndpoint by EndpointName in ResourceGroup</span></span>

### <span data-ttu-id="41cfc-115">Przykład 3. Pobierz obiekt AzDigitalTwinsEndpoint za pomocą obiektu "AzDigitalTwinsEndpoint"</span><span class="sxs-lookup"><span data-stu-id="41cfc-115">Example 3: Get AzDigitalTwinsEndpoint by 'AzDigitalTwinsEndpoint' Object</span></span>
```powershell
PS C:\> $GetAzDigitalTwinsEndpoint = Get-AzDigitalTwinsEndpoint -EndpointName youriDigitalTwinEndpoint -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest
Get-AzDigitalTwinsEndpoint -InputObject $GetAzDigitalTwinsEndpoint

Name                     Type
----                     ----
youriDigitalTwinEndpoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="41cfc-116">Uzyskiwanie witryny AzDigitalTwinsEndpoint przez obiekt "AzDigitalTwinsEndpoint"</span><span class="sxs-lookup"><span data-stu-id="41cfc-116">Get AzDigitalTwinsEndpoint by 'AzDigitalTwinsEndpoint' Object</span></span>

## <span data-ttu-id="41cfc-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="41cfc-117">PARAMETERS</span></span>

### <span data-ttu-id="41cfc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41cfc-118">-DefaultProfile</span></span>
<span data-ttu-id="41cfc-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="41cfc-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41cfc-120">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="41cfc-120">-EndpointName</span></span>
<span data-ttu-id="41cfc-121">Nazwa zasobu punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="41cfc-121">Name of Endpoint Resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41cfc-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="41cfc-122">-InputObject</span></span>
<span data-ttu-id="41cfc-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="41cfc-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="41cfc-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41cfc-124">-ResourceGroupName</span></span>
<span data-ttu-id="41cfc-125">Nazwa grupy zasobów zawierającej nazwę DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="41cfc-125">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41cfc-126">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="41cfc-126">-ResourceName</span></span>
<span data-ttu-id="41cfc-127">Nazwa pliku DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="41cfc-127">The name of the DigitalTwinsInstance.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41cfc-128">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="41cfc-128">-SubscriptionId</span></span>
<span data-ttu-id="41cfc-129">Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="41cfc-129">The subscription identifier.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41cfc-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41cfc-130">CommonParameters</span></span>
<span data-ttu-id="41cfc-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41cfc-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41cfc-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="41cfc-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41cfc-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="41cfc-133">INPUTS</span></span>

### <span data-ttu-id="41cfc-134">Microsoft.Azure.PowerShell.Cmdlet.DigitalTwins.Models.IDigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="41cfc-134">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span></span>

## <span data-ttu-id="41cfc-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="41cfc-135">OUTPUTS</span></span>

### <span data-ttu-id="41cfc-136">Microsoft.Azure.PowerShell.Cmdlet.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span><span class="sxs-lookup"><span data-stu-id="41cfc-136">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span></span>

## <span data-ttu-id="41cfc-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="41cfc-137">NOTES</span></span>

<span data-ttu-id="41cfc-138">ALIASY</span><span class="sxs-lookup"><span data-stu-id="41cfc-138">ALIASES</span></span>

<span data-ttu-id="41cfc-139">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="41cfc-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="41cfc-140">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="41cfc-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="41cfc-141">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="41cfc-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="41cfc-142">INPUTOBJECT: <IDigitalTwinsIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="41cfc-142">INPUTOBJECT <IDigitalTwinsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="41cfc-143">`[EndpointName <String>]`: Nazwa zasobu punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="41cfc-143">`[EndpointName <String>]`: Name of Endpoint Resource.</span></span>
  - <span data-ttu-id="41cfc-144">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="41cfc-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="41cfc-145">`[Location <String>]`: Lokalizacja technologii DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="41cfc-145">`[Location <String>]`: Location of DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="41cfc-146">`[ResourceGroupName <String>]`: nazwa grupy zasobów zawierającej nazwę DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="41cfc-146">`[ResourceGroupName <String>]`: The name of the resource group that contains the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="41cfc-147">`[ResourceName <String>]`: nazwa pliku DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="41cfc-147">`[ResourceName <String>]`: The name of the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="41cfc-148">`[SubscriptionId <String>]`: Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="41cfc-148">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="41cfc-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="41cfc-149">RELATED LINKS</span></span>

