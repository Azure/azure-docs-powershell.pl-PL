---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.digitaltwins/get-azdigitaltwinsendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Get-AzDigitalTwinsEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Get-AzDigitalTwinsEndpoint.md
ms.openlocfilehash: 6299fcc8828031b61aabc912fcd30c1ed8cbb0e2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98376873"
---
# <span data-ttu-id="f32de-101">Get-AzDigitalTwinsEndpoint</span><span class="sxs-lookup"><span data-stu-id="f32de-101">Get-AzDigitalTwinsEndpoint</span></span>

## <span data-ttu-id="f32de-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f32de-102">SYNOPSIS</span></span>
<span data-ttu-id="f32de-103">Uzyskaj punkt końcowy DigitalTwinsInstances.</span><span class="sxs-lookup"><span data-stu-id="f32de-103">Get DigitalTwinsInstances Endpoint.</span></span>

## <span data-ttu-id="f32de-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f32de-104">SYNTAX</span></span>

### <span data-ttu-id="f32de-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="f32de-105">List (Default)</span></span>
```
Get-AzDigitalTwinsEndpoint -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f32de-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="f32de-106">Get</span></span>
```
Get-AzDigitalTwinsEndpoint -EndpointName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f32de-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f32de-107">GetViaIdentity</span></span>
```
Get-AzDigitalTwinsEndpoint -InputObject <IDigitalTwinsIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="f32de-108">Opis</span><span class="sxs-lookup"><span data-stu-id="f32de-108">DESCRIPTION</span></span>
<span data-ttu-id="f32de-109">Uzyskaj punkt końcowy DigitalTwinsInstances.</span><span class="sxs-lookup"><span data-stu-id="f32de-109">Get DigitalTwinsInstances Endpoint.</span></span>

## <span data-ttu-id="f32de-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f32de-110">EXAMPLES</span></span>

### <span data-ttu-id="f32de-111">Przykład 1: Lista AzDigitalTwinsEndpoint w obszarze zasobów</span><span class="sxs-lookup"><span data-stu-id="f32de-111">Example 1: List AzDigitalTwinsEndpoint in ResourceGroup</span></span>
```powershell
PS C:\> Get-AzDigitalTwinsEndpoint -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest

Name                     Type
----                     ----
youriDigitalTwinEndpoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="f32de-112">Lista wszystkich AzDigitalTwinsEndpoints według ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f32de-112">List all AzDigitalTwinsEndpoints by ResourceGroupName</span></span>

### <span data-ttu-id="f32de-113">Przykład 2: Get AzDigitalTwinsEndpoint według punktu Końcowegoname</span><span class="sxs-lookup"><span data-stu-id="f32de-113">Example 2: Get AzDigitalTwinsEndpoint by EndpointName</span></span>
```powershell
PS C:\> Get-AzDigitalTwinsEndpoint -EndpointName youriDigitalTwinEndpoint -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest

Name                     Type
----                     ----
youriDigitalTwinEndpoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="f32de-114">Pobierz AzDigitalTwinsEndpoint według punktu końcowego w obszarze zasobów</span><span class="sxs-lookup"><span data-stu-id="f32de-114">Get AzDigitalTwinsEndpoint by EndpointName in ResourceGroup</span></span>

### <span data-ttu-id="f32de-115">Przykład 3: pobieranie AzDigitalTwinsEndpoint według obiektu "AzDigitalTwinsEndpoint"</span><span class="sxs-lookup"><span data-stu-id="f32de-115">Example 3: Get AzDigitalTwinsEndpoint by 'AzDigitalTwinsEndpoint' Object</span></span>
```powershell
PS C:\> $GetAzDigitalTwinsEndpoint = Get-AzDigitalTwinsEndpoint -EndpointName youriDigitalTwinEndpoint -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest
Get-AzDigitalTwinsEndpoint -InputObject $GetAzDigitalTwinsEndpoint

Name                     Type
----                     ----
youriDigitalTwinEndpoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="f32de-116">AzDigitalTwinsEndpoint według obiektu "AzDigitalTwinsEndpoint"</span><span class="sxs-lookup"><span data-stu-id="f32de-116">Get AzDigitalTwinsEndpoint by 'AzDigitalTwinsEndpoint' Object</span></span>

## <span data-ttu-id="f32de-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f32de-117">PARAMETERS</span></span>

### <span data-ttu-id="f32de-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f32de-118">-DefaultProfile</span></span>
<span data-ttu-id="f32de-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f32de-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f32de-120">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="f32de-120">-EndpointName</span></span>
<span data-ttu-id="f32de-121">Nazwa zasobu punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="f32de-121">Name of Endpoint Resource.</span></span>

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

### <span data-ttu-id="f32de-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f32de-122">-InputObject</span></span>
<span data-ttu-id="f32de-123">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="f32de-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f32de-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f32de-124">-ResourceGroupName</span></span>
<span data-ttu-id="f32de-125">Nazwa grupy zasobów zawierającej DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="f32de-125">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="f32de-126">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="f32de-126">-ResourceName</span></span>
<span data-ttu-id="f32de-127">Nazwa DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="f32de-127">The name of the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="f32de-128">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="f32de-128">-SubscriptionId</span></span>
<span data-ttu-id="f32de-129">Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="f32de-129">The subscription identifier.</span></span>

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

### <span data-ttu-id="f32de-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f32de-130">CommonParameters</span></span>
<span data-ttu-id="f32de-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f32de-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f32de-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f32de-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f32de-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f32de-133">INPUTS</span></span>

### <span data-ttu-id="f32de-134">Microsoft. Azure. PowerShell. polecenia. DigitalTwins. models. IDigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="f32de-134">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span></span>

## <span data-ttu-id="f32de-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f32de-135">OUTPUTS</span></span>

### <span data-ttu-id="f32de-136">Microsoft. Azure. PowerShell. polecenia. DigitalTwins. models. Api20201031. IDigitalTwinsEndpointResource</span><span class="sxs-lookup"><span data-stu-id="f32de-136">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span></span>

## <span data-ttu-id="f32de-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f32de-137">NOTES</span></span>

<span data-ttu-id="f32de-138">PISUJE</span><span class="sxs-lookup"><span data-stu-id="f32de-138">ALIASES</span></span>

<span data-ttu-id="f32de-139">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f32de-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f32de-140">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="f32de-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f32de-141">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f32de-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f32de-142">INPUTobject <IDigitalTwinsIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="f32de-142">INPUTOBJECT <IDigitalTwinsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f32de-143">`[EndpointName <String>]`: Nazwa zasobu punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="f32de-143">`[EndpointName <String>]`: Name of Endpoint Resource.</span></span>
  - <span data-ttu-id="f32de-144">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="f32de-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f32de-145">`[Location <String>]`: Lokalizacja DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="f32de-145">`[Location <String>]`: Location of DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="f32de-146">`[ResourceGroupName <String>]`: Nazwa grupy zasobów zawierającej DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="f32de-146">`[ResourceGroupName <String>]`: The name of the resource group that contains the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="f32de-147">`[ResourceName <String>]`: Nazwa DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="f32de-147">`[ResourceName <String>]`: The name of the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="f32de-148">`[SubscriptionId <String>]`: Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="f32de-148">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="f32de-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f32de-149">RELATED LINKS</span></span>

