---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/powershell/module/az.digitaltwins/new-azdigitaltwinsinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsInstance.md
ms.openlocfilehash: 54fdbcfe83dd93101030d92f9f3eec19d1a2564f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984936"
---
# <span data-ttu-id="06fad-101">New-AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="06fad-101">New-AzDigitalTwinsInstance</span></span>

## <span data-ttu-id="06fad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06fad-102">SYNOPSIS</span></span>
<span data-ttu-id="06fad-103">Tworzenie lub aktualizowanie metadanych pliku DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="06fad-103">Create or update the metadata of a DigitalTwinsInstance.</span></span>
<span data-ttu-id="06fad-104">Zwykłym wzorcem modyfikowania właściwości jest pobieranie metadanych DigitalTwinsInstance i zabezpieczeń, a następnie łączenie ich z wartościami zmodyfikowanymi w nowej treści w celu zaktualizowania pliku DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="06fad-104">The usual pattern to modify a property is to retrieve the DigitalTwinsInstance and security metadata, and then combine them with the modified values in a new body to update the DigitalTwinsInstance.</span></span>

## <span data-ttu-id="06fad-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="06fad-105">SYNTAX</span></span>

### <span data-ttu-id="06fad-106">CreateExpanded (Default)</span><span class="sxs-lookup"><span data-stu-id="06fad-106">CreateExpanded (Default)</span></span>
```
New-AzDigitalTwinsInstance -ResourceGroupName <String> -ResourceName <String> -Location <String>
 [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="06fad-107">Tworzenie</span><span class="sxs-lookup"><span data-stu-id="06fad-107">Create</span></span>
```
New-AzDigitalTwinsInstance -ResourceGroupName <String> -ResourceName <String>
 -DigitalTwinsCreate <IDigitalTwinsDescription> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="06fad-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="06fad-108">DESCRIPTION</span></span>
<span data-ttu-id="06fad-109">Tworzenie lub aktualizowanie metadanych pliku DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="06fad-109">Create or update the metadata of a DigitalTwinsInstance.</span></span>
<span data-ttu-id="06fad-110">Zwykłym wzorcem modyfikowania właściwości jest pobieranie metadanych DigitalTwinsInstance i zabezpieczeń, a następnie łączenie ich z wartościami zmodyfikowanymi w nowej treści w celu zaktualizowania pliku DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="06fad-110">The usual pattern to modify a property is to retrieve the DigitalTwinsInstance and security metadata, and then combine them with the modified values in a new body to update the DigitalTwinsInstance.</span></span>

## <span data-ttu-id="06fad-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="06fad-111">EXAMPLES</span></span>

### <span data-ttu-id="06fad-112">Przykład 1. Domyślnie utwórz element AzDigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="06fad-112">Example 1: Create an AzDigitalTwinsInstance by default.</span></span>
```powershell
PS C:\> New-AzDigitalTwinsInstance -ResourceGroupName youritest -ResourceName youriDigitalTwin -Location eastus

Location Name             SkuName Type
-------- ----             ------- ----
eastus   youriDigitalTwin S1      Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="06fad-113">Domyślnie utwórz element AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="06fad-113">Create an AzDigitalTwinsInstance by default</span></span>

### <span data-ttu-id="06fad-114">Przykład 2. Tworzenie obiektu AzDigitalTwinsInstance przez obiekt AzDigitalTwins.</span><span class="sxs-lookup"><span data-stu-id="06fad-114">Example 2: Create an AzDigitalTwinsInstance by AzDigitalTwins Object.</span></span>
```powershell
PS C:\> $GetAzDigTwin = Get-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest
New-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest01 -DigitalTwinsCreate $getAzdigitalTwins

Location Name                    Type
-------- ----                    ----
eastus   youriDigitalTwinsTest01 Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="06fad-115">Tworzenie obiektu AzDigitalTwinsInstance przez obiekt AzDigitalTwins</span><span class="sxs-lookup"><span data-stu-id="06fad-115">Create an AzDigitalTwinsInstance by AzDigitalTwins Object</span></span>

## <span data-ttu-id="06fad-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="06fad-116">PARAMETERS</span></span>

### <span data-ttu-id="06fad-117">— AsJob</span><span class="sxs-lookup"><span data-stu-id="06fad-117">-AsJob</span></span>
<span data-ttu-id="06fad-118">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="06fad-118">Run the command as a job</span></span>

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

### <span data-ttu-id="06fad-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06fad-119">-DefaultProfile</span></span>
<span data-ttu-id="06fad-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="06fad-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06fad-121">-DigitalTwinsCreate</span><span class="sxs-lookup"><span data-stu-id="06fad-121">-DigitalTwinsCreate</span></span>
<span data-ttu-id="06fad-122">Opis usługi DigitalTwins.</span><span class="sxs-lookup"><span data-stu-id="06fad-122">The description of the DigitalTwins service.</span></span>
<span data-ttu-id="06fad-123">Aby skonstruować, zobacz sekcję NOTES, aby uzyskać informacje o właściwościach DIGITALTWINSCREATE i utworzyć tabelę skrótów.</span><span class="sxs-lookup"><span data-stu-id="06fad-123">To construct, see NOTES section for DIGITALTWINSCREATE properties and create a hash table.</span></span>

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

### <span data-ttu-id="06fad-124">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="06fad-124">-Location</span></span>
<span data-ttu-id="06fad-125">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="06fad-125">The resource location.</span></span>

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

### <span data-ttu-id="06fad-126">-NoWait</span><span class="sxs-lookup"><span data-stu-id="06fad-126">-NoWait</span></span>
<span data-ttu-id="06fad-127">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="06fad-127">Run the command asynchronously</span></span>

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

### <span data-ttu-id="06fad-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06fad-128">-ResourceGroupName</span></span>
<span data-ttu-id="06fad-129">Nazwa grupy zasobów zawierającej nazwę DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="06fad-129">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="06fad-130">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="06fad-130">-ResourceName</span></span>
<span data-ttu-id="06fad-131">Nazwa pliku DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="06fad-131">The name of the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="06fad-132">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="06fad-132">-SubscriptionId</span></span>
<span data-ttu-id="06fad-133">Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="06fad-133">The subscription identifier.</span></span>

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

### <span data-ttu-id="06fad-134">— Tag</span><span class="sxs-lookup"><span data-stu-id="06fad-134">-Tag</span></span>
<span data-ttu-id="06fad-135">Tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="06fad-135">The resource tags.</span></span>

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

### <span data-ttu-id="06fad-136">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="06fad-136">-Confirm</span></span>
<span data-ttu-id="06fad-137">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="06fad-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06fad-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06fad-138">-WhatIf</span></span>
<span data-ttu-id="06fad-139">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06fad-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06fad-140">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="06fad-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06fad-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06fad-141">CommonParameters</span></span>
<span data-ttu-id="06fad-142">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06fad-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06fad-143">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="06fad-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06fad-144">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="06fad-144">INPUTS</span></span>

### <span data-ttu-id="06fad-145">Microsoft.Azure.PowerShell.Cmdlet.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span><span class="sxs-lookup"><span data-stu-id="06fad-145">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span></span>

## <span data-ttu-id="06fad-146">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="06fad-146">OUTPUTS</span></span>

### <span data-ttu-id="06fad-147">Microsoft.Azure.PowerShell.Cmdlet.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span><span class="sxs-lookup"><span data-stu-id="06fad-147">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span></span>

## <span data-ttu-id="06fad-148">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="06fad-148">NOTES</span></span>

<span data-ttu-id="06fad-149">ALIASY</span><span class="sxs-lookup"><span data-stu-id="06fad-149">ALIASES</span></span>

<span data-ttu-id="06fad-150">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="06fad-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="06fad-151">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="06fad-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="06fad-152">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="06fad-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="06fad-153">DIGITALTWINSCREATE: <IDigitalTwinsDescription> Opis usługi DigitalTwins.</span><span class="sxs-lookup"><span data-stu-id="06fad-153">DIGITALTWINSCREATE <IDigitalTwinsDescription>: The description of the DigitalTwins service.</span></span>
  - <span data-ttu-id="06fad-154">`Location <String>`: lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="06fad-154">`Location <String>`: The resource location.</span></span>
  - <span data-ttu-id="06fad-155">`[Tag <IDigitalTwinsResourceTags>]`: Tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="06fad-155">`[Tag <IDigitalTwinsResourceTags>]`: The resource tags.</span></span>
    - <span data-ttu-id="06fad-156">`[(Any) <String>]`: Wskazuje to, że do tego obiektu można dodać dowolną właściwość.</span><span class="sxs-lookup"><span data-stu-id="06fad-156">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>

## <span data-ttu-id="06fad-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="06fad-157">RELATED LINKS</span></span>

