---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.digitaltwins/get-azdigitaltwinsinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Get-AzDigitalTwinsInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Get-AzDigitalTwinsInstance.md
ms.openlocfilehash: 17e036128dcc6c43044a83d2bbc254cc994ae508
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100237949"
---
# <span data-ttu-id="83235-101">Get-AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="83235-101">Get-AzDigitalTwinsInstance</span></span>

## <span data-ttu-id="83235-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83235-102">SYNOPSIS</span></span>
<span data-ttu-id="83235-103">Pobierz zasób DigitalTwinsInstances.</span><span class="sxs-lookup"><span data-stu-id="83235-103">Get DigitalTwinsInstances resource.</span></span>

## <span data-ttu-id="83235-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="83235-104">SYNTAX</span></span>

### <span data-ttu-id="83235-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="83235-105">List (Default)</span></span>
```
Get-AzDigitalTwinsInstance [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="83235-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="83235-106">Get</span></span>
```
Get-AzDigitalTwinsInstance -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="83235-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="83235-107">GetViaIdentity</span></span>
```
Get-AzDigitalTwinsInstance -InputObject <IDigitalTwinsIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="83235-108">Lista1</span><span class="sxs-lookup"><span data-stu-id="83235-108">List1</span></span>
```
Get-AzDigitalTwinsInstance -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="83235-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="83235-109">DESCRIPTION</span></span>
<span data-ttu-id="83235-110">Pobierz zasób DigitalTwinsInstances.</span><span class="sxs-lookup"><span data-stu-id="83235-110">Get DigitalTwinsInstances resource.</span></span>

## <span data-ttu-id="83235-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="83235-111">EXAMPLES</span></span>

### <span data-ttu-id="83235-112">Przykład 1. Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="83235-112">Example 1: List (Default)</span></span>
```powershell
PS C:\> Get-AzDigitalTwinsInstance

Location Name                    Type
-------- ----                    ----
eastus   youriDigitalTwinsTest   Microsoft.DigitalTwins/digitalTwinsInstances
eastus   youriDigitalTwin        Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="83235-113">Domyślnie pobierz wszystkie ustawienia DigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="83235-113">Get all the DigitalTwinsInstance by default</span></span>

### <span data-ttu-id="83235-114">Przykład 2. Pobierz</span><span class="sxs-lookup"><span data-stu-id="83235-114">Example 2: Get</span></span>
```powershell
PS C:\> Get-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwin

Location Name             Type
-------- ----             ----
eastus   youriDigitalTwin Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="83235-115">Uzyskiwanie określonego parametru AzDigitalTwinsInstance według nazwy zasobu</span><span class="sxs-lookup"><span data-stu-id="83235-115">Get the specified AzDigitalTwinsInstance by ResourceName</span></span>

### <span data-ttu-id="83235-116">Przykład 3. GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="83235-116">Example 3: GetViaIdentity</span></span>
```powershell
PS C:\> $NewAzDigital = New-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwin -Location eastus
Get-AzDigitalTwinsInstance -inputObject $NewAzDigital

Location Name             Type
-------- ----             ----
eastus   youriDigitalTwin Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="83235-117">Uzyskiwanie określonego obiektu AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="83235-117">Get the specified AzDigitalTwinsInstance by Object</span></span>

### <span data-ttu-id="83235-118">Przykład 4. Lista1</span><span class="sxs-lookup"><span data-stu-id="83235-118">Example 4: List1</span></span>
```powershell
PS C:\> Get-AzDigitalTwinsInstance -ResourceGroupName youritemp

Location Name                    Type
-------- ----                    ----
eastus   youriDigitalTwinsTest   Microsoft.DigitalTwins/digitalTwinsInstances
eastus   youriDigitalTwin        Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="83235-119">Uzyskiwanie wszystkich rekordów DigitalTwinsInstance według nazwy ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83235-119">Get all the DigitalTwinsInstance by ResourceGroupName</span></span>

## <span data-ttu-id="83235-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="83235-120">PARAMETERS</span></span>

### <span data-ttu-id="83235-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83235-121">-DefaultProfile</span></span>
<span data-ttu-id="83235-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="83235-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83235-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="83235-123">-InputObject</span></span>
<span data-ttu-id="83235-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="83235-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="83235-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83235-125">-ResourceGroupName</span></span>
<span data-ttu-id="83235-126">Nazwa grupy zasobów zawierającej nazwę DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="83235-126">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="83235-127">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="83235-127">-ResourceName</span></span>
<span data-ttu-id="83235-128">Nazwa pliku DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="83235-128">The name of the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="83235-129">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="83235-129">-SubscriptionId</span></span>
<span data-ttu-id="83235-130">Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="83235-130">The subscription identifier.</span></span>

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

### <span data-ttu-id="83235-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83235-131">CommonParameters</span></span>
<span data-ttu-id="83235-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83235-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83235-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="83235-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83235-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="83235-134">INPUTS</span></span>

### <span data-ttu-id="83235-135">Microsoft.Azure.PowerShell.Cmdlet.DigitalTwins.Models.IDigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="83235-135">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span></span>

## <span data-ttu-id="83235-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="83235-136">OUTPUTS</span></span>

### <span data-ttu-id="83235-137">Microsoft.Azure.PowerShell.Cmdlet.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span><span class="sxs-lookup"><span data-stu-id="83235-137">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span></span>

## <span data-ttu-id="83235-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="83235-138">NOTES</span></span>

<span data-ttu-id="83235-139">ALIASY</span><span class="sxs-lookup"><span data-stu-id="83235-139">ALIASES</span></span>

<span data-ttu-id="83235-140">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="83235-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="83235-141">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="83235-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="83235-142">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="83235-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="83235-143">INPUTOBJECT: <IDigitalTwinsIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="83235-143">INPUTOBJECT <IDigitalTwinsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="83235-144">`[EndpointName <String>]`: Nazwa zasobu punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="83235-144">`[EndpointName <String>]`: Name of Endpoint Resource.</span></span>
  - <span data-ttu-id="83235-145">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="83235-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="83235-146">`[Location <String>]`: Lokalizacja technologii DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="83235-146">`[Location <String>]`: Location of DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="83235-147">`[ResourceGroupName <String>]`: nazwa grupy zasobów zawierającej nazwę DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="83235-147">`[ResourceGroupName <String>]`: The name of the resource group that contains the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="83235-148">`[ResourceName <String>]`: nazwa pliku DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="83235-148">`[ResourceName <String>]`: The name of the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="83235-149">`[SubscriptionId <String>]`: Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="83235-149">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="83235-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="83235-150">RELATED LINKS</span></span>

