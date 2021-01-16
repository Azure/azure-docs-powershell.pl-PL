---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.digitaltwins/get-azdigitaltwinsendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Get-AzDigitalTwinsEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Get-AzDigitalTwinsEndpoint.md
ms.openlocfilehash: 6299fcc8828031b61aabc912fcd30c1ed8cbb0e2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98347041"
---
# <span data-ttu-id="ce01f-101">Get-AzDigitalTwinsEndpoint</span><span class="sxs-lookup"><span data-stu-id="ce01f-101">Get-AzDigitalTwinsEndpoint</span></span>

## <span data-ttu-id="ce01f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ce01f-102">SYNOPSIS</span></span>
<span data-ttu-id="ce01f-103">Uzyskaj punkt końcowy DigitalTwinsInstances.</span><span class="sxs-lookup"><span data-stu-id="ce01f-103">Get DigitalTwinsInstances Endpoint.</span></span>

## <span data-ttu-id="ce01f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ce01f-104">SYNTAX</span></span>

### <span data-ttu-id="ce01f-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="ce01f-105">List (Default)</span></span>
```
Get-AzDigitalTwinsEndpoint -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ce01f-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="ce01f-106">Get</span></span>
```
Get-AzDigitalTwinsEndpoint -EndpointName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ce01f-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ce01f-107">GetViaIdentity</span></span>
```
Get-AzDigitalTwinsEndpoint -InputObject <IDigitalTwinsIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="ce01f-108">Opis</span><span class="sxs-lookup"><span data-stu-id="ce01f-108">DESCRIPTION</span></span>
<span data-ttu-id="ce01f-109">Uzyskaj punkt końcowy DigitalTwinsInstances.</span><span class="sxs-lookup"><span data-stu-id="ce01f-109">Get DigitalTwinsInstances Endpoint.</span></span>

## <span data-ttu-id="ce01f-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ce01f-110">EXAMPLES</span></span>

### <span data-ttu-id="ce01f-111">Przykład 1: Lista AzDigitalTwinsEndpoint w obszarze zasobów</span><span class="sxs-lookup"><span data-stu-id="ce01f-111">Example 1: List AzDigitalTwinsEndpoint in ResourceGroup</span></span>
```powershell
PS C:\> Get-AzDigitalTwinsEndpoint -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest

Name                     Type
----                     ----
youriDigitalTwinEndpoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="ce01f-112">Lista wszystkich AzDigitalTwinsEndpoints według ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce01f-112">List all AzDigitalTwinsEndpoints by ResourceGroupName</span></span>

### <span data-ttu-id="ce01f-113">Przykład 2: Get AzDigitalTwinsEndpoint według punktu Końcowegoname</span><span class="sxs-lookup"><span data-stu-id="ce01f-113">Example 2: Get AzDigitalTwinsEndpoint by EndpointName</span></span>
```powershell
PS C:\> Get-AzDigitalTwinsEndpoint -EndpointName youriDigitalTwinEndpoint -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest

Name                     Type
----                     ----
youriDigitalTwinEndpoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="ce01f-114">Pobierz AzDigitalTwinsEndpoint według punktu końcowego w obszarze zasobów</span><span class="sxs-lookup"><span data-stu-id="ce01f-114">Get AzDigitalTwinsEndpoint by EndpointName in ResourceGroup</span></span>

### <span data-ttu-id="ce01f-115">Przykład 3: pobieranie AzDigitalTwinsEndpoint według obiektu "AzDigitalTwinsEndpoint"</span><span class="sxs-lookup"><span data-stu-id="ce01f-115">Example 3: Get AzDigitalTwinsEndpoint by 'AzDigitalTwinsEndpoint' Object</span></span>
```powershell
PS C:\> $GetAzDigitalTwinsEndpoint = Get-AzDigitalTwinsEndpoint -EndpointName youriDigitalTwinEndpoint -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest
Get-AzDigitalTwinsEndpoint -InputObject $GetAzDigitalTwinsEndpoint

Name                     Type
----                     ----
youriDigitalTwinEndpoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="ce01f-116">AzDigitalTwinsEndpoint według obiektu "AzDigitalTwinsEndpoint"</span><span class="sxs-lookup"><span data-stu-id="ce01f-116">Get AzDigitalTwinsEndpoint by 'AzDigitalTwinsEndpoint' Object</span></span>

## <span data-ttu-id="ce01f-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ce01f-117">PARAMETERS</span></span>

### <span data-ttu-id="ce01f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce01f-118">-DefaultProfile</span></span>
<span data-ttu-id="ce01f-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ce01f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ce01f-120">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="ce01f-120">-EndpointName</span></span>
<span data-ttu-id="ce01f-121">Nazwa zasobu punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="ce01f-121">Name of Endpoint Resource.</span></span>

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

### <span data-ttu-id="ce01f-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ce01f-122">-InputObject</span></span>
<span data-ttu-id="ce01f-123">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="ce01f-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ce01f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce01f-124">-ResourceGroupName</span></span>
<span data-ttu-id="ce01f-125">Nazwa grupy zasobów zawierającej DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="ce01f-125">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="ce01f-126">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="ce01f-126">-ResourceName</span></span>
<span data-ttu-id="ce01f-127">Nazwa DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="ce01f-127">The name of the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="ce01f-128">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="ce01f-128">-SubscriptionId</span></span>
<span data-ttu-id="ce01f-129">Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="ce01f-129">The subscription identifier.</span></span>

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

### <span data-ttu-id="ce01f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce01f-130">CommonParameters</span></span>
<span data-ttu-id="ce01f-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce01f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce01f-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ce01f-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce01f-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ce01f-133">INPUTS</span></span>

### <span data-ttu-id="ce01f-134">Microsoft. Azure. PowerShell. polecenia. DigitalTwins. models. IDigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="ce01f-134">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span></span>

## <span data-ttu-id="ce01f-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ce01f-135">OUTPUTS</span></span>

### <span data-ttu-id="ce01f-136">Microsoft. Azure. PowerShell. polecenia. DigitalTwins. models. Api20201031. IDigitalTwinsEndpointResource</span><span class="sxs-lookup"><span data-stu-id="ce01f-136">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span></span>

## <span data-ttu-id="ce01f-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ce01f-137">NOTES</span></span>

<span data-ttu-id="ce01f-138">PISUJE</span><span class="sxs-lookup"><span data-stu-id="ce01f-138">ALIASES</span></span>

<span data-ttu-id="ce01f-139">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ce01f-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ce01f-140">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="ce01f-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ce01f-141">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ce01f-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ce01f-142">INPUTobject <IDigitalTwinsIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="ce01f-142">INPUTOBJECT <IDigitalTwinsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ce01f-143">`[EndpointName <String>]`: Nazwa zasobu punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="ce01f-143">`[EndpointName <String>]`: Name of Endpoint Resource.</span></span>
  - <span data-ttu-id="ce01f-144">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="ce01f-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ce01f-145">`[Location <String>]`: Lokalizacja DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="ce01f-145">`[Location <String>]`: Location of DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="ce01f-146">`[ResourceGroupName <String>]`: Nazwa grupy zasobów zawierającej DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="ce01f-146">`[ResourceGroupName <String>]`: The name of the resource group that contains the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="ce01f-147">`[ResourceName <String>]`: Nazwa DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="ce01f-147">`[ResourceName <String>]`: The name of the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="ce01f-148">`[SubscriptionId <String>]`: Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="ce01f-148">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="ce01f-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ce01f-149">RELATED LINKS</span></span>

