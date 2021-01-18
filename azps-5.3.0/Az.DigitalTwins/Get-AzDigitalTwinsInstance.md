---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.digitaltwins/get-azdigitaltwinsinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Get-AzDigitalTwinsInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Get-AzDigitalTwinsInstance.md
ms.openlocfilehash: 17e036128dcc6c43044a83d2bbc254cc994ae508
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98499145"
---
# <span data-ttu-id="80953-101">Get-AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="80953-101">Get-AzDigitalTwinsInstance</span></span>

## <span data-ttu-id="80953-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="80953-102">SYNOPSIS</span></span>
<span data-ttu-id="80953-103">Pobierz zasób DigitalTwinsInstances.</span><span class="sxs-lookup"><span data-stu-id="80953-103">Get DigitalTwinsInstances resource.</span></span>

## <span data-ttu-id="80953-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="80953-104">SYNTAX</span></span>

### <span data-ttu-id="80953-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="80953-105">List (Default)</span></span>
```
Get-AzDigitalTwinsInstance [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="80953-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="80953-106">Get</span></span>
```
Get-AzDigitalTwinsInstance -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="80953-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="80953-107">GetViaIdentity</span></span>
```
Get-AzDigitalTwinsInstance -InputObject <IDigitalTwinsIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="80953-108">List1</span><span class="sxs-lookup"><span data-stu-id="80953-108">List1</span></span>
```
Get-AzDigitalTwinsInstance -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="80953-109">Opis</span><span class="sxs-lookup"><span data-stu-id="80953-109">DESCRIPTION</span></span>
<span data-ttu-id="80953-110">Pobierz zasób DigitalTwinsInstances.</span><span class="sxs-lookup"><span data-stu-id="80953-110">Get DigitalTwinsInstances resource.</span></span>

## <span data-ttu-id="80953-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="80953-111">EXAMPLES</span></span>

### <span data-ttu-id="80953-112">Przykład 1: lista (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="80953-112">Example 1: List (Default)</span></span>
```powershell
PS C:\> Get-AzDigitalTwinsInstance

Location Name                    Type
-------- ----                    ----
eastus   youriDigitalTwinsTest   Microsoft.DigitalTwins/digitalTwinsInstances
eastus   youriDigitalTwin        Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="80953-113">Domyślnie Pobierz wszystkie DigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="80953-113">Get all the DigitalTwinsInstance by default</span></span>

### <span data-ttu-id="80953-114">Przykład 2: Uzyskaj</span><span class="sxs-lookup"><span data-stu-id="80953-114">Example 2: Get</span></span>
```powershell
PS C:\> Get-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwin

Location Name             Type
-------- ----             ----
eastus   youriDigitalTwin Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="80953-115">Pobierz określoną AzDigitalTwinsInstance przez resourceName</span><span class="sxs-lookup"><span data-stu-id="80953-115">Get the specified AzDigitalTwinsInstance by ResourceName</span></span>

### <span data-ttu-id="80953-116">Przykład 3: GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="80953-116">Example 3: GetViaIdentity</span></span>
```powershell
PS C:\> $NewAzDigital = New-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwin -Location eastus
Get-AzDigitalTwinsInstance -inputObject $NewAzDigital

Location Name             Type
-------- ----             ----
eastus   youriDigitalTwin Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="80953-117">Pobieranie określonego AzDigitalTwinsInstance według obiektu</span><span class="sxs-lookup"><span data-stu-id="80953-117">Get the specified AzDigitalTwinsInstance by Object</span></span>

### <span data-ttu-id="80953-118">Przykład 4: list1</span><span class="sxs-lookup"><span data-stu-id="80953-118">Example 4: List1</span></span>
```powershell
PS C:\> Get-AzDigitalTwinsInstance -ResourceGroupName youritemp

Location Name                    Type
-------- ----                    ----
eastus   youriDigitalTwinsTest   Microsoft.DigitalTwins/digitalTwinsInstances
eastus   youriDigitalTwin        Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="80953-119">Pobierz wszystkie DigitalTwinsInstance przez ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80953-119">Get all the DigitalTwinsInstance by ResourceGroupName</span></span>

## <span data-ttu-id="80953-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="80953-120">PARAMETERS</span></span>

### <span data-ttu-id="80953-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80953-121">-DefaultProfile</span></span>
<span data-ttu-id="80953-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="80953-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="80953-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="80953-123">-InputObject</span></span>
<span data-ttu-id="80953-124">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="80953-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="80953-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80953-125">-ResourceGroupName</span></span>
<span data-ttu-id="80953-126">Nazwa grupy zasobów zawierającej DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="80953-126">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="80953-127">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="80953-127">-ResourceName</span></span>
<span data-ttu-id="80953-128">Nazwa DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="80953-128">The name of the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="80953-129">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="80953-129">-SubscriptionId</span></span>
<span data-ttu-id="80953-130">Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="80953-130">The subscription identifier.</span></span>

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

### <span data-ttu-id="80953-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80953-131">CommonParameters</span></span>
<span data-ttu-id="80953-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80953-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80953-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="80953-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80953-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="80953-134">INPUTS</span></span>

### <span data-ttu-id="80953-135">Microsoft. Azure. PowerShell. polecenia. DigitalTwins. models. IDigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="80953-135">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span></span>

## <span data-ttu-id="80953-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="80953-136">OUTPUTS</span></span>

### <span data-ttu-id="80953-137">Microsoft. Azure. PowerShell. polecenia. DigitalTwins. models. Api20201031. IDigitalTwinsDescription</span><span class="sxs-lookup"><span data-stu-id="80953-137">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span></span>

## <span data-ttu-id="80953-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="80953-138">NOTES</span></span>

<span data-ttu-id="80953-139">PISUJE</span><span class="sxs-lookup"><span data-stu-id="80953-139">ALIASES</span></span>

<span data-ttu-id="80953-140">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="80953-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="80953-141">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="80953-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="80953-142">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="80953-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="80953-143">INPUTobject <IDigitalTwinsIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="80953-143">INPUTOBJECT <IDigitalTwinsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="80953-144">`[EndpointName <String>]`: Nazwa zasobu punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="80953-144">`[EndpointName <String>]`: Name of Endpoint Resource.</span></span>
  - <span data-ttu-id="80953-145">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="80953-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="80953-146">`[Location <String>]`: Lokalizacja DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="80953-146">`[Location <String>]`: Location of DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="80953-147">`[ResourceGroupName <String>]`: Nazwa grupy zasobów zawierającej DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="80953-147">`[ResourceGroupName <String>]`: The name of the resource group that contains the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="80953-148">`[ResourceName <String>]`: Nazwa DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="80953-148">`[ResourceName <String>]`: The name of the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="80953-149">`[SubscriptionId <String>]`: Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="80953-149">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="80953-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="80953-150">RELATED LINKS</span></span>

