---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.digitaltwins/new-azdigitaltwinsinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsInstance.md
ms.openlocfilehash: d6a748897b956759ad64056b0d9b83a6e82e91fc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98499141"
---
# <span data-ttu-id="ea22d-101">New-AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="ea22d-101">New-AzDigitalTwinsInstance</span></span>

## <span data-ttu-id="ea22d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ea22d-102">SYNOPSIS</span></span>
<span data-ttu-id="ea22d-103">Utwórz lub zaktualizuj metadane DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="ea22d-103">Create or update the metadata of a DigitalTwinsInstance.</span></span>
<span data-ttu-id="ea22d-104">Typowym wzorcem do modyfikowania właściwości jest pobranie metadanych DigitalTwinsInstance i zabezpieczeń, a następnie połączenie ich z wartościami zmienionymi w nowej treści w celu zaktualizowania DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="ea22d-104">The usual pattern to modify a property is to retrieve the DigitalTwinsInstance and security metadata, and then combine them with the modified values in a new body to update the DigitalTwinsInstance.</span></span>

## <span data-ttu-id="ea22d-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ea22d-105">SYNTAX</span></span>

### <span data-ttu-id="ea22d-106">Rozszerzenie (domyślne)</span><span class="sxs-lookup"><span data-stu-id="ea22d-106">CreateExpanded (Default)</span></span>
```
New-AzDigitalTwinsInstance -ResourceGroupName <String> -ResourceName <String> -Location <String>
 [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ea22d-107">Tworzonych</span><span class="sxs-lookup"><span data-stu-id="ea22d-107">Create</span></span>
```
New-AzDigitalTwinsInstance -ResourceGroupName <String> -ResourceName <String>
 -DigitalTwinsCreate <IDigitalTwinsDescription> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ea22d-108">Opis</span><span class="sxs-lookup"><span data-stu-id="ea22d-108">DESCRIPTION</span></span>
<span data-ttu-id="ea22d-109">Utwórz lub zaktualizuj metadane DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="ea22d-109">Create or update the metadata of a DigitalTwinsInstance.</span></span>
<span data-ttu-id="ea22d-110">Typowym wzorcem do modyfikowania właściwości jest pobranie metadanych DigitalTwinsInstance i zabezpieczeń, a następnie połączenie ich z wartościami zmienionymi w nowej treści w celu zaktualizowania DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="ea22d-110">The usual pattern to modify a property is to retrieve the DigitalTwinsInstance and security metadata, and then combine them with the modified values in a new body to update the DigitalTwinsInstance.</span></span>

## <span data-ttu-id="ea22d-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ea22d-111">EXAMPLES</span></span>

### <span data-ttu-id="ea22d-112">Przykład 1: domyślnie Utwórz AzDigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="ea22d-112">Example 1: Create an AzDigitalTwinsInstance by default.</span></span>
```powershell
PS C:\> New-AzDigitalTwinsInstance -ResourceGroupName youritest -ResourceName youriDigitalTwin -Location eastus

Location Name             SkuName Type
-------- ----             ------- ----
eastus   youriDigitalTwin S1      Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="ea22d-113">Domyślnie Utwórz AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="ea22d-113">Create an AzDigitalTwinsInstance by default</span></span>

### <span data-ttu-id="ea22d-114">Przykład 2: Tworzenie AzDigitalTwinsInstance za pomocą obiektu AzDigitalTwins.</span><span class="sxs-lookup"><span data-stu-id="ea22d-114">Example 2: Create an AzDigitalTwinsInstance by AzDigitalTwins Object.</span></span>
```powershell
PS C:\> $GetAzDigTwin = Get-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest
New-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest01 -DigitalTwinsCreate $getAzdigitalTwins

Location Name                    Type
-------- ----                    ----
eastus   youriDigitalTwinsTest01 Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="ea22d-115">Tworzenie AzDigitalTwinsInstance za pomocą obiektu AzDigitalTwins</span><span class="sxs-lookup"><span data-stu-id="ea22d-115">Create an AzDigitalTwinsInstance by AzDigitalTwins Object</span></span>

## <span data-ttu-id="ea22d-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ea22d-116">PARAMETERS</span></span>

### <span data-ttu-id="ea22d-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ea22d-117">-AsJob</span></span>
<span data-ttu-id="ea22d-118">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="ea22d-118">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea22d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea22d-119">-DefaultProfile</span></span>
<span data-ttu-id="ea22d-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ea22d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea22d-121">-DigitalTwinsCreate</span><span class="sxs-lookup"><span data-stu-id="ea22d-121">-DigitalTwinsCreate</span></span>
<span data-ttu-id="ea22d-122">Opis usługi DigitalTwins.</span><span class="sxs-lookup"><span data-stu-id="ea22d-122">The description of the DigitalTwins service.</span></span>
<span data-ttu-id="ea22d-123">Aby skonstruować, zobacz sekcję notatki dla właściwości DIGITALTWINSCREATE i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="ea22d-123">To construct, see NOTES section for DIGITALTWINSCREATE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription
Parameter Sets: Create
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ea22d-124">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="ea22d-124">-Location</span></span>
<span data-ttu-id="ea22d-125">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="ea22d-125">The resource location.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea22d-126">-Nowait</span><span class="sxs-lookup"><span data-stu-id="ea22d-126">-NoWait</span></span>
<span data-ttu-id="ea22d-127">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="ea22d-127">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea22d-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea22d-128">-ResourceGroupName</span></span>
<span data-ttu-id="ea22d-129">Nazwa grupy zasobów zawierającej DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="ea22d-129">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea22d-130">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="ea22d-130">-ResourceName</span></span>
<span data-ttu-id="ea22d-131">Nazwa DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="ea22d-131">The name of the DigitalTwinsInstance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea22d-132">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="ea22d-132">-SubscriptionId</span></span>
<span data-ttu-id="ea22d-133">Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="ea22d-133">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea22d-134">-Tag</span><span class="sxs-lookup"><span data-stu-id="ea22d-134">-Tag</span></span>
<span data-ttu-id="ea22d-135">Znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="ea22d-135">The resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea22d-136">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ea22d-136">-Confirm</span></span>
<span data-ttu-id="ea22d-137">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea22d-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea22d-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea22d-138">-WhatIf</span></span>
<span data-ttu-id="ea22d-139">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea22d-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea22d-140">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ea22d-140">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea22d-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea22d-141">CommonParameters</span></span>
<span data-ttu-id="ea22d-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea22d-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea22d-143">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ea22d-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea22d-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ea22d-144">INPUTS</span></span>

### <span data-ttu-id="ea22d-145">Microsoft. Azure. PowerShell. polecenia. DigitalTwins. models. Api20201031. IDigitalTwinsDescription</span><span class="sxs-lookup"><span data-stu-id="ea22d-145">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span></span>

## <span data-ttu-id="ea22d-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ea22d-146">OUTPUTS</span></span>

### <span data-ttu-id="ea22d-147">Microsoft. Azure. PowerShell. polecenia. DigitalTwins. models. Api20201031. IDigitalTwinsDescription</span><span class="sxs-lookup"><span data-stu-id="ea22d-147">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span></span>

## <span data-ttu-id="ea22d-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ea22d-148">NOTES</span></span>

<span data-ttu-id="ea22d-149">PISUJE</span><span class="sxs-lookup"><span data-stu-id="ea22d-149">ALIASES</span></span>

<span data-ttu-id="ea22d-150">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ea22d-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ea22d-151">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="ea22d-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ea22d-152">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ea22d-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ea22d-153">DIGITALTWINSCREATE <IDigitalTwinsDescription> : Opis usługi DigitalTwins.</span><span class="sxs-lookup"><span data-stu-id="ea22d-153">DIGITALTWINSCREATE <IDigitalTwinsDescription>: The description of the DigitalTwins service.</span></span>
  - <span data-ttu-id="ea22d-154">`Location <String>`: Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="ea22d-154">`Location <String>`: The resource location.</span></span>
  - <span data-ttu-id="ea22d-155">`[Tag <IDigitalTwinsResourceTags>]`: Znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="ea22d-155">`[Tag <IDigitalTwinsResourceTags>]`: The resource tags.</span></span>
    - <span data-ttu-id="ea22d-156">`[(Any) <String>]`: Wskazuje, że do tego obiektu można dodać dowolną właściwość.</span><span class="sxs-lookup"><span data-stu-id="ea22d-156">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>

## <span data-ttu-id="ea22d-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ea22d-157">RELATED LINKS</span></span>

