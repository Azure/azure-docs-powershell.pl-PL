---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 18D5B95E-4CF1-4C79-AE8B-9F4DA49B46A9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/add-azurermlogprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmLogProfile.md
ms.openlocfilehash: 0ef53015b3e07eeb69cdcfd0ab70c67317ab92cd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553672"
---
# <span data-ttu-id="f041d-101">Add-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="f041d-101">Add-AzureRmLogProfile</span></span>

## <span data-ttu-id="f041d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f041d-102">SYNOPSIS</span></span>
<span data-ttu-id="f041d-103">Tworzy nowy profil dziennika aktywności.</span><span class="sxs-lookup"><span data-stu-id="f041d-103">Creates a new activity log profile.</span></span> <span data-ttu-id="f041d-104">Ten profil służy do archiwizowania dziennika aktywności na koncie usługi Azure Storage lub przesyłania strumieniowego do centrum zdarzeń platformy Azure w ramach tej samej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="f041d-104">This profile is used to either archive the activity log to an Azure storage account or stream it to an Azure event hub in the same subscription.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f041d-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f041d-105">SYNTAX</span></span>

```
Add-AzureRmLogProfile -Name <String> [-StorageAccountId <String>] [-ServiceBusRuleId <String>]
 [-RetentionInDays <Int32>] -Location <System.Collections.Generic.List`1[System.String]>
 [-Category <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f041d-106">Opis</span><span class="sxs-lookup"><span data-stu-id="f041d-106">DESCRIPTION</span></span>
<span data-ttu-id="f041d-107">Polecenie cmdlet **Add-AzureRmLogProfile** tworzy profil dziennika.</span><span class="sxs-lookup"><span data-stu-id="f041d-107">The **Add-AzureRmLogProfile** cmdlet creates a log profile.</span></span>

- <span data-ttu-id="f041d-108">**Konto magazynu** — obsługiwane jest tylko standardowe konto magazynu (konto magazynu Premium jest nieobsługiwane).</span><span class="sxs-lookup"><span data-stu-id="f041d-108">**Storage Account** - Only standard storage account (premium storage account is not supported) is supported.</span></span> <span data-ttu-id="f041d-109">Być może jest to typ ARM lub klasyczny.</span><span class="sxs-lookup"><span data-stu-id="f041d-109">It could either be of type ARM or Classic.</span></span> <span data-ttu-id="f041d-110">Jeśli jest on zarejestrowany na koncie magazynu, koszty przechowywania dziennika aktywności są rozliczane według zwykłych standardowych stawek za składowanie.</span><span class="sxs-lookup"><span data-stu-id="f041d-110">If it's logged to a storage account, the cost of storing the activity log is billed at normal standard storage rates.</span></span> <span data-ttu-id="f041d-111">Tylko jeden profil dziennika dla jednej subskrypcji może zawierać tylko jedno konto magazynu na jedną subskrypcję, aby wyeksportować dziennik aktywności.</span><span class="sxs-lookup"><span data-stu-id="f041d-111">There could be only one log profile per subscription consequentially only one storage account per subscription can be used to export activity log.</span></span> 

- <span data-ttu-id="f041d-112">**Centrum zdarzeń** — tylko jeden profil dziennika dla jednej subskrypcji może mieć tylko jeden centrum zdarzeń na subskrypcję, aby wyeksportować dziennik aktywności.</span><span class="sxs-lookup"><span data-stu-id="f041d-112">**Event Hub** - There could be only one log profile per subscription consequentially only one event hub per subscription can be used to export activity log.</span></span> <span data-ttu-id="f041d-113">Jeśli dziennik aktywności jest przesyłany strumieniowo do centrum zdarzeń, będą obowiązywać standardowe ceny centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="f041d-113">If activity log is streamed to an event hub, standard event hub pricing will apply.</span></span> 

<span data-ttu-id="f041d-114">Zdarzenia w dzienniku aktywności mogą dotyczyć regionu lub mogą być "globalnymi".</span><span class="sxs-lookup"><span data-stu-id="f041d-114">In the activity log, events can pertain to a region or could be "Global".</span></span> <span data-ttu-id="f041d-115">Globalnym względnie oznacza, że te zdarzenia są regionem agnostics i są niezależne od regionu, w rzeczywistości większość wydarzeń należy do tej kategorii.</span><span class="sxs-lookup"><span data-stu-id="f041d-115">Global essentially means these events are region agnostics and are independent of region, in fact majority of events fall into this category.</span></span> <span data-ttu-id="f041d-116">Jeśli profil dziennika aktywności jest ustawiony na podstawie portalu, domyślnie dodawany jest komunikat "globalny" wraz z dowolnym innym regionem wybranym w interfejsie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="f041d-116">If the activity log profile is set from the portal, it implicitly adds "Global" along with any other region selected in the user interface.</span></span> <span data-ttu-id="f041d-117">W przypadku korzystania z polecenia cmdlet lokalizacja "Global" musi być jawnie wymieniona poza dowolnym innym regionem.</span><span class="sxs-lookup"><span data-stu-id="f041d-117">When using the cmdlet, the location as "Global" must be explicitly mentioned apart from any other region.</span></span> 

<span data-ttu-id="f041d-118">**Uwaga** : w **przypadku niepowodzenia ustawienia "globalne" w lokalizacjach nie będzie można eksportować dziennika aktywności.**</span><span class="sxs-lookup"><span data-stu-id="f041d-118">**Note** :- **Failing to set "Global" in the locations will result in a majority of activity log not getting exported.**</span></span> 

<span data-ttu-id="f041d-119">To polecenie cmdlet implementuje wzorzec ShouldProcess, tzn. może zażądać potwierdzenia od użytkownika przed faktycznym utworzeniem, zmodyfikowaniem lub usunięciem zasobu.</span><span class="sxs-lookup"><span data-stu-id="f041d-119">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="f041d-120">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f041d-120">EXAMPLES</span></span>

### <span data-ttu-id="f041d-121">Przykład 1: Dodawanie nowego profilu dziennika w celu wyeksportowania dziennika aktywności zgodnego z warunkiem lokalizacji do konta magazynu</span><span class="sxs-lookup"><span data-stu-id="f041d-121">Example 1 : Add a new log profile to export the activity log matching the location condition to a storage account</span></span>
```
Add-AzureRmLogProfile -Locations "Global","West US" -Name ExportLogProfile -StorageAccountId /subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount
```

## <span data-ttu-id="f041d-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f041d-122">PARAMETERS</span></span>

### <span data-ttu-id="f041d-123">-Category</span><span class="sxs-lookup"><span data-stu-id="f041d-123">-Category</span></span>
<span data-ttu-id="f041d-124">Określa listę kategorii.</span><span class="sxs-lookup"><span data-stu-id="f041d-124">Specifies the list of categories.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: Categories

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f041d-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f041d-125">-DefaultProfile</span></span>
<span data-ttu-id="f041d-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="f041d-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f041d-127">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="f041d-127">-Location</span></span>
<span data-ttu-id="f041d-128">Określa lokalizację profilu dziennika.</span><span class="sxs-lookup"><span data-stu-id="f041d-128">Specifies the location of the log profile.</span></span>
<span data-ttu-id="f041d-129">Prawidłowe wartości: Uruchom polecenie cmdlet poniżej, aby pobrać najnowszą listę lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="f041d-129">Valid values: Run below cmdlet to get the latest list of locations.</span></span> 

<span data-ttu-id="f041d-130">Get-AzureLocation | Wybieranie parametru DisplayName</span><span class="sxs-lookup"><span data-stu-id="f041d-130">Get-AzureLocation | Select DisplayName</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: Locations

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f041d-131">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f041d-131">-Name</span></span>
<span data-ttu-id="f041d-132">Określa nazwę profilu.</span><span class="sxs-lookup"><span data-stu-id="f041d-132">Specifies the name of the profile.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f041d-133">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="f041d-133">-RetentionInDays</span></span>
<span data-ttu-id="f041d-134">Określa zasady przechowywania w dniach.</span><span class="sxs-lookup"><span data-stu-id="f041d-134">Specifies the retention policy, in days.</span></span> <span data-ttu-id="f041d-135">Jest to liczba dni, w których dzienniki są zachowywane na określonym koncie magazynu.</span><span class="sxs-lookup"><span data-stu-id="f041d-135">This is the number of days the logs are preserved in the storage account specified.</span></span> <span data-ttu-id="f041d-136">Aby zachować dane w nieskończoność, ustaw **wartość 0**.</span><span class="sxs-lookup"><span data-stu-id="f041d-136">To retain the data forever set this to **0**.</span></span> <span data-ttu-id="f041d-137">Jeśli nie jest określony, domyślnie przyjmowana jest **wartość 0**.</span><span class="sxs-lookup"><span data-stu-id="f041d-137">If it's not specified, then it defaults to **0**.</span></span> <span data-ttu-id="f041d-138">Do przechowywania danych będą stosowane zwykłe stawki za połączenia w standardowym magazynie lub w centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="f041d-138">Normal standard storage or event hub billing rates will apply for data retention.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f041d-139">-ServiceBusRuleId</span><span class="sxs-lookup"><span data-stu-id="f041d-139">-ServiceBusRuleId</span></span>
<span data-ttu-id="f041d-140">Określa identyfikator reguły magistrali usług.</span><span class="sxs-lookup"><span data-stu-id="f041d-140">Specifies the ID of the Service Bus rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f041d-141">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="f041d-141">-StorageAccountId</span></span>
<span data-ttu-id="f041d-142">Określa identyfikator konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="f041d-142">Specifies the ID of the Storage account.</span></span> <span data-ttu-id="f041d-143">Identyfikator to w pełni kwalifikowany identyfikator zasobów konta magazynu, na przykład</span><span class="sxs-lookup"><span data-stu-id="f041d-143">ID is the fully qualified Resource ID of the storage account for example</span></span>  

<span data-ttu-id="f041d-144">/subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount</span><span class="sxs-lookup"><span data-stu-id="f041d-144">/subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f041d-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f041d-145">CommonParameters</span></span>
<span data-ttu-id="f041d-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f041d-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f041d-147">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f041d-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f041d-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f041d-148">INPUTS</span></span>

### <span data-ttu-id="f041d-149">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="f041d-149">None</span></span>
<span data-ttu-id="f041d-150">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="f041d-150">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f041d-151">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f041d-151">OUTPUTS</span></span>

### <span data-ttu-id="f041d-152">Microsoft. Azure. Commands. Insights. OutputClasses. PSLogProfile</span><span class="sxs-lookup"><span data-stu-id="f041d-152">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile</span></span>

## <span data-ttu-id="f041d-153">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f041d-153">NOTES</span></span>

## <span data-ttu-id="f041d-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f041d-154">RELATED LINKS</span></span>

[<span data-ttu-id="f041d-155">Get-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="f041d-155">Get-AzureRmLogProfile</span></span>](./Get-AzureRmLogProfile.md)

[<span data-ttu-id="f041d-156">Remove-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="f041d-156">Remove-AzureRmLogProfile</span></span>](./Remove-AzureRmLogProfile.md)


