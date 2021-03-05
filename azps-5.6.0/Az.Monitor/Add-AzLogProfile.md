---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 18D5B95E-4CF1-4C79-AE8B-9F4DA49B46A9
online version: https://docs.microsoft.com/powershell/module/az.monitor/add-azlogprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzLogProfile.md
ms.openlocfilehash: a5d60cbda668e963793dbb350950ea0e85812892
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980321"
---
# <span data-ttu-id="2d721-101">Add-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="2d721-101">Add-AzLogProfile</span></span>

## <span data-ttu-id="2d721-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d721-102">SYNOPSIS</span></span>
<span data-ttu-id="2d721-103">Tworzy nowy profil dziennika aktywności.</span><span class="sxs-lookup"><span data-stu-id="2d721-103">Creates a new activity log profile.</span></span> <span data-ttu-id="2d721-104">Ten profil służy do archiwizowania dziennika aktywności na koncie magazynu platformy Azure lub strumieniowego przesyłania go do centrum zdarzeń platformy Azure w tej samej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="2d721-104">This profile is used to either archive the activity log to an Azure storage account or stream it to an Azure event hub in the same subscription.</span></span> 

## <span data-ttu-id="2d721-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2d721-105">SYNTAX</span></span>

```
Add-AzLogProfile -Name <String> [-StorageAccountId <String>] [-ServiceBusRuleId <String>]
 [-RetentionInDays <Int32>] -Location <System.Collections.Generic.List`1[System.String]>
 [-Category <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d721-106">OPIS</span><span class="sxs-lookup"><span data-stu-id="2d721-106">DESCRIPTION</span></span>
<span data-ttu-id="2d721-107">Polecenie **cmdlet Add-AzLogProfile** tworzy profil dziennika.</span><span class="sxs-lookup"><span data-stu-id="2d721-107">The **Add-AzLogProfile** cmdlet creates a log profile.</span></span>
- <span data-ttu-id="2d721-108">**Konto magazynu** — obsługiwane jest tylko standardowe konto magazynu (konto magazynu premium nie jest obsługiwane).</span><span class="sxs-lookup"><span data-stu-id="2d721-108">**Storage Account** - Only standard storage account (premium storage account is not supported) is supported.</span></span> <span data-ttu-id="2d721-109">Może to być typ ARM klasyczny.</span><span class="sxs-lookup"><span data-stu-id="2d721-109">It could either be of type ARM or Classic.</span></span> <span data-ttu-id="2d721-110">Jeśli jest on zalogowany na koncie magazynu, koszt przechowywania dziennika działań jest rozliczany przy normalnych standardowych stawkach przestrzeni dyskowej.</span><span class="sxs-lookup"><span data-stu-id="2d721-110">If it's logged to a storage account, the cost of storing the activity log is billed at normal standard storage rates.</span></span> <span data-ttu-id="2d721-111">W konsekwencji do wyeksportowania dziennika aktywności może być użyte tylko jedno konto magazynu na subskrypcję.</span><span class="sxs-lookup"><span data-stu-id="2d721-111">There could be only one log profile per subscription consequentially only one storage account per subscription can be used to export activity log.</span></span> 
- <span data-ttu-id="2d721-112">**Centrum zdarzeń** — w ramach jednej subskrypcji może być tylko jeden profil dziennika, w konsekwencji tylko jedno centrum zdarzeń na subskrypcję może zostać użyte do wyeksportowania dziennika aktywności.</span><span class="sxs-lookup"><span data-stu-id="2d721-112">**Event Hub** - There could be only one log profile per subscription consequentially only one event hub per subscription can be used to export activity log.</span></span> <span data-ttu-id="2d721-113">Jeśli dziennik aktywności jest przesyłany strumieniowo do centrum zdarzeń, będą obowiązywały standardowe ceny w centrum wydarzeń.</span><span class="sxs-lookup"><span data-stu-id="2d721-113">If activity log is streamed to an event hub, standard event hub pricing will apply.</span></span> <span data-ttu-id="2d721-114">W dzienniku aktywności zdarzenia mogą dotyczyć regionu lub mogą być "globalne".</span><span class="sxs-lookup"><span data-stu-id="2d721-114">In the activity log, events can pertain to a region or could be "Global".</span></span> <span data-ttu-id="2d721-115">Globalnie oznacza, że te zdarzenia są agnostykami regionów i są niezależne od regionu, w rzeczywistości większość zdarzeń należy do tej kategorii.</span><span class="sxs-lookup"><span data-stu-id="2d721-115">Global essentially means these events are region agnostics and are independent of region, in fact majority of events fall into this category.</span></span> <span data-ttu-id="2d721-116">Jeśli profil dziennika aktywności jest ustawiony w portalu, niejawnie dodaje on wartość "Global" wraz z dowolnym innym regionem wybranym w interfejsie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="2d721-116">If the activity log profile is set from the portal, it implicitly adds "Global" along with any other region selected in the user interface.</span></span> <span data-ttu-id="2d721-117">Podczas korzystania z polecenia cmdlet należy jawnie wspomnieć o lokalizacji jako "globalnej" poza dowolnym innym regionem.</span><span class="sxs-lookup"><span data-stu-id="2d721-117">When using the cmdlet, the location as "Global" must be explicitly mentioned apart from any other region.</span></span> 
<span data-ttu-id="2d721-118">**Uwaga** :- Jeśli nie ustawisz w lokalizacjach ustawienia **"Globalna",** większość dziennika aktywności nie zostanie wyeksportowana.</span><span class="sxs-lookup"><span data-stu-id="2d721-118">**Note** :- **Failing to set "Global" in the locations will result in a majority of activity log not getting exported.**</span></span> <span data-ttu-id="2d721-119">To polecenie cmdlet implementuje wzorzec ShouldProcess, czyli może wymagać potwierdzenia od użytkownika przed utworzeniem, zmodyfikowaniem lub usunięciem zasobu.</span><span class="sxs-lookup"><span data-stu-id="2d721-119">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="2d721-120">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2d721-120">EXAMPLES</span></span>

### <span data-ttu-id="2d721-121">Przykład 1. Dodawanie nowego profilu dziennika w celu wyeksportowania dziennika aktywności spełniającego warunek lokalizacji do konta magazynu</span><span class="sxs-lookup"><span data-stu-id="2d721-121">Example 1: Add a new log profile to export the activity log matching the location condition to a storage account</span></span>
```powershell
Add-AzLogProfile -Location "Global","West US" -Name ExportLogProfile -StorageAccountId /subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount
```

### <span data-ttu-id="2d721-122">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="2d721-122">Example 2</span></span>

<span data-ttu-id="2d721-123">Tworzy nowy profil dziennika aktywności.</span><span class="sxs-lookup"><span data-stu-id="2d721-123">Creates a new activity log profile.</span></span> <span data-ttu-id="2d721-124">(wygenerowane automatycznie)</span><span class="sxs-lookup"><span data-stu-id="2d721-124">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Add-AzLogProfile -Location 'Global' -Name ExportLogProfile -RetentionInDays <Int32> -ServiceBusRuleId <String> -StorageAccountId /subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount
```

## <span data-ttu-id="2d721-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2d721-125">PARAMETERS</span></span>

### <span data-ttu-id="2d721-126">— Kategoria</span><span class="sxs-lookup"><span data-stu-id="2d721-126">-Category</span></span>
<span data-ttu-id="2d721-127">Określa listę kategorii.</span><span class="sxs-lookup"><span data-stu-id="2d721-127">Specifies the list of categories.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d721-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d721-128">-DefaultProfile</span></span>
<span data-ttu-id="2d721-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="2d721-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2d721-130">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="2d721-130">-Location</span></span>
<span data-ttu-id="2d721-131">Określa lokalizację profilu dziennika.</span><span class="sxs-lookup"><span data-stu-id="2d721-131">Specifies the location of the log profile.</span></span>
<span data-ttu-id="2d721-132">Prawidłowe wartości: Uruchom poniżej polecenia cmdlet, aby uzyskać najnowszą listę lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="2d721-132">Valid values: Run below cmdlet to get the latest list of locations.</span></span> <span data-ttu-id="2d721-133">Get-AzLocation | Wybierz pozycję DisplayName (Nazwa wyświetlana)</span><span class="sxs-lookup"><span data-stu-id="2d721-133">Get-AzLocation | Select DisplayName</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d721-134">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="2d721-134">-Name</span></span>
<span data-ttu-id="2d721-135">Określa nazwę profilu.</span><span class="sxs-lookup"><span data-stu-id="2d721-135">Specifies the name of the profile.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d721-136">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="2d721-136">-RetentionInDays</span></span>
<span data-ttu-id="2d721-137">Określa zasady przechowywania w dniach.</span><span class="sxs-lookup"><span data-stu-id="2d721-137">Specifies the retention policy, in days.</span></span> <span data-ttu-id="2d721-138">Jest to liczba dni zachowywania dzienników na określonym koncie magazynu.</span><span class="sxs-lookup"><span data-stu-id="2d721-138">This is the number of days the logs are preserved in the storage account specified.</span></span> <span data-ttu-id="2d721-139">Aby zachować dane na zawsze, ustaw wartość **0.**</span><span class="sxs-lookup"><span data-stu-id="2d721-139">To retain the data forever set this to **0**.</span></span> <span data-ttu-id="2d721-140">Jeśli nie zostanie określone, wartość domyślna to **0.**</span><span class="sxs-lookup"><span data-stu-id="2d721-140">If it's not specified, then it defaults to **0**.</span></span> <span data-ttu-id="2d721-141">W przypadku przechowywania danych będą obowiązywały standardowe stawki za przechowywanie danych w centrum wydarzeń lub magazynu standardowego.</span><span class="sxs-lookup"><span data-stu-id="2d721-141">Normal standard storage or event hub billing rates will apply for data retention.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d721-142">-ServiceBusRuleId</span><span class="sxs-lookup"><span data-stu-id="2d721-142">-ServiceBusRuleId</span></span>
<span data-ttu-id="2d721-143">Określa identyfikator reguły autobusu usług.</span><span class="sxs-lookup"><span data-stu-id="2d721-143">Specifies the ID of the Service Bus rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d721-144">- StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="2d721-144">-StorageAccountId</span></span>
<span data-ttu-id="2d721-145">Określa identyfikator konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="2d721-145">Specifies the ID of the Storage account.</span></span> <span data-ttu-id="2d721-146">Identyfikator jest w pełni kwalifikowanym identyfikatorem zasobu konta magazynu, na przykład</span><span class="sxs-lookup"><span data-stu-id="2d721-146">ID is the fully qualified Resource ID of the storage account for example</span></span>  
<span data-ttu-id="2d721-147">/subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount</span><span class="sxs-lookup"><span data-stu-id="2d721-147">/subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d721-148">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2d721-148">-Confirm</span></span>
<span data-ttu-id="2d721-149">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="2d721-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d721-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d721-150">-WhatIf</span></span>
<span data-ttu-id="2d721-151">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2d721-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2d721-152">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="2d721-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d721-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d721-153">CommonParameters</span></span>
<span data-ttu-id="2d721-154">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d721-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d721-155">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2d721-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d721-156">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2d721-156">INPUTS</span></span>

### <span data-ttu-id="2d721-157">System.String</span><span class="sxs-lookup"><span data-stu-id="2d721-157">System.String</span></span>

### <span data-ttu-id="2d721-158">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="2d721-158">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="2d721-159">System.Collections.Generic.List'1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="2d721-159">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="2d721-160">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2d721-160">OUTPUTS</span></span>

### <span data-ttu-id="2d721-161">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile</span><span class="sxs-lookup"><span data-stu-id="2d721-161">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile</span></span>

## <span data-ttu-id="2d721-162">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2d721-162">NOTES</span></span>

## <span data-ttu-id="2d721-163">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2d721-163">RELATED LINKS</span></span>

[<span data-ttu-id="2d721-164">Get-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="2d721-164">Get-AzLogProfile</span></span>](./Get-AzLogProfile.md)

[<span data-ttu-id="2d721-165">Remove-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="2d721-165">Remove-AzLogProfile</span></span>](./Remove-AzLogProfile.md)


