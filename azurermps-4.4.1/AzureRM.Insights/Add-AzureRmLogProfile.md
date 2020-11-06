---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 18D5B95E-4CF1-4C79-AE8B-9F4DA49B46A9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmLogProfile.md
ms.openlocfilehash: 40efc9e6afbb4f1424fcbcfe70e3376eb9ab5a23
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553870"
---
# <span data-ttu-id="3a9d8-101">Add-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="3a9d8-101">Add-AzureRmLogProfile</span></span>

## <span data-ttu-id="3a9d8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3a9d8-102">SYNOPSIS</span></span>
<span data-ttu-id="3a9d8-103">Tworzy nowy profil dziennika aktywności.</span><span class="sxs-lookup"><span data-stu-id="3a9d8-103">Creates a new activity log profile.</span></span> <span data-ttu-id="3a9d8-104">Ten profil służy do archiwizowania dziennika aktywności na koncie usługi Azure Storage lub przesyłania strumieniowego do centrum zdarzeń platformy Azure w ramach tej samej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="3a9d8-104">This profile is used to either archive the activity log to an Azure storage account or stream it to an Azure event hub in the same subscription.</span></span> 

- <span data-ttu-id="3a9d8-105">**Konto magazynu** — obsługiwane jest tylko standardowe konto magazynu (konto magazynu Premium jest nieobsługiwane).</span><span class="sxs-lookup"><span data-stu-id="3a9d8-105">**Storage Account** - Only standard storage account (premium storage account is not supported) is supported.</span></span> <span data-ttu-id="3a9d8-106">Być może jest to typ ARM lub klasyczny.</span><span class="sxs-lookup"><span data-stu-id="3a9d8-106">It could either be of type ARM or Classic.</span></span> <span data-ttu-id="3a9d8-107">Jeśli jest on zarejestrowany na koncie magazynu, koszty przechowywania dziennika aktywności są rozliczane według zwykłych standardowych stawek za składowanie.</span><span class="sxs-lookup"><span data-stu-id="3a9d8-107">If it's logged to a storage account, the cost of storing the activity log is billed at normal standard storage rates.</span></span> <span data-ttu-id="3a9d8-108">Tylko jeden profil dziennika dla jednej subskrypcji może zawierać tylko jedno konto magazynu na jedną subskrypcję, aby wyeksportować dziennik aktywności.</span><span class="sxs-lookup"><span data-stu-id="3a9d8-108">There could be only one log profile per subscription consequentially only one storage account per subscription can be used to export activity log.</span></span> 

- <span data-ttu-id="3a9d8-109">**Centrum zdarzeń** — tylko jeden profil dziennika dla jednej subskrypcji może mieć tylko jeden centrum zdarzeń na subskrypcję, aby wyeksportować dziennik aktywności.</span><span class="sxs-lookup"><span data-stu-id="3a9d8-109">**Event Hub** - There could be only one log profile per subscription consequentially only one event hub per subscription can be used to export activity log.</span></span> <span data-ttu-id="3a9d8-110">Jeśli dziennik aktywności jest przesyłany strumieniowo do centrum zdarzeń, będą obowiązywać standardowe ceny centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="3a9d8-110">If activity log is streamed to an event hub, standard event hub pricing will apply.</span></span> 

<span data-ttu-id="3a9d8-111">Zdarzenia w dzienniku aktywności mogą dotyczyć regionu lub mogą być "globalnymi".</span><span class="sxs-lookup"><span data-stu-id="3a9d8-111">In the activity log, events can pertain to a region or could be "Global".</span></span> <span data-ttu-id="3a9d8-112">Globalnym względnie oznacza, że te zdarzenia są regionem agnostics i są niezależne od regionu, w rzeczywistości większość wydarzeń należy do tej kategorii.</span><span class="sxs-lookup"><span data-stu-id="3a9d8-112">Global essentially means these events are region agnostics and are independent of region, in fact majority of events fall into this category.</span></span> <span data-ttu-id="3a9d8-113">Jeśli profil dziennika aktywności jest ustawiony na podstawie portalu, domyślnie dodawany jest komunikat "globalny" wraz z dowolnym innym regionem wybranym w interfejsie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="3a9d8-113">If the activity log profile is set from the portal, it implicitly adds "Global" along with any other region selected in the user interface.</span></span> <span data-ttu-id="3a9d8-114">W przypadku korzystania z polecenia cmdlet lokalizacja "Global" musi być jawnie wymieniona poza dowolnym innym regionem.</span><span class="sxs-lookup"><span data-stu-id="3a9d8-114">When using the cmdlet, the location as "Global" must be explicitly mentioned apart from any other region.</span></span> 

<span data-ttu-id="3a9d8-115">**Uwaga** : w **przypadku niepowodzenia ustawienia "globalne" w lokalizacjach nie będzie można eksportować dziennika aktywności.**</span><span class="sxs-lookup"><span data-stu-id="3a9d8-115">**Note** :- **Failing to set "Global" in the locations will result in a majority of activity log not getting exported.**</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3a9d8-116">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3a9d8-116">SYNTAX</span></span>

```
Add-AzureRmLogProfile -Name <String> [-StorageAccountId <String>] [-ServiceBusRuleId <String>]
 [-RetentionInDays <Int32>] -Locations <System.Collections.Generic.List`1[System.String]>
 [-Categories <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3a9d8-117">Opis</span><span class="sxs-lookup"><span data-stu-id="3a9d8-117">DESCRIPTION</span></span>
<span data-ttu-id="3a9d8-118">Polecenie cmdlet **Add-AzureRmLogProfile** tworzy profil dziennika.</span><span class="sxs-lookup"><span data-stu-id="3a9d8-118">The **Add-AzureRmLogProfile** cmdlet creates a log profile.</span></span>

## <span data-ttu-id="3a9d8-119">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3a9d8-119">EXAMPLES</span></span>

### <span data-ttu-id="3a9d8-120">Przykład 1: Dodawanie nowego profilu dziennika w celu wyeksportowania dziennika aktywności zgodnego z warunkiem lokalizacji do konta magazynu</span><span class="sxs-lookup"><span data-stu-id="3a9d8-120">Example 1 : Add a new log profile to export the activity log matching the location condition to a storage account</span></span>
```
Add-AzureRmLogProfile -Locations "Global","West US" -Name ExportLogProfile -StorageAccountId /subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount
```

## <span data-ttu-id="3a9d8-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3a9d8-121">PARAMETERS</span></span>

### <span data-ttu-id="3a9d8-122">-Kategorie</span><span class="sxs-lookup"><span data-stu-id="3a9d8-122">-Categories</span></span>
<span data-ttu-id="3a9d8-123">Określa listę kategorii.</span><span class="sxs-lookup"><span data-stu-id="3a9d8-123">Specifies the list of categories.</span></span>

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

### <span data-ttu-id="3a9d8-124">— Lokalizacje</span><span class="sxs-lookup"><span data-stu-id="3a9d8-124">-Locations</span></span>
<span data-ttu-id="3a9d8-125">Określa lokalizację profilu dziennika.</span><span class="sxs-lookup"><span data-stu-id="3a9d8-125">Specifies the location of the log profile.</span></span>
<span data-ttu-id="3a9d8-126">Prawidłowe wartości: Uruchom polecenie cmdlet poniżej, aby pobrać najnowszą listę lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="3a9d8-126">Valid values: Run below cmdlet to get the latest list of locations.</span></span> 

<span data-ttu-id="3a9d8-127">Get-AzureLocation | Wybieranie parametru DisplayName</span><span class="sxs-lookup"><span data-stu-id="3a9d8-127">Get-AzureLocation | Select DisplayName</span></span>

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

### <span data-ttu-id="3a9d8-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3a9d8-128">-Name</span></span>
<span data-ttu-id="3a9d8-129">Określa nazwę profilu.</span><span class="sxs-lookup"><span data-stu-id="3a9d8-129">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="3a9d8-130">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="3a9d8-130">-RetentionInDays</span></span>
<span data-ttu-id="3a9d8-131">Określa zasady przechowywania w dniach.</span><span class="sxs-lookup"><span data-stu-id="3a9d8-131">Specifies the retention policy, in days.</span></span> <span data-ttu-id="3a9d8-132">Jest to liczba dni, w których dzienniki są zachowywane na określonym koncie magazynu.</span><span class="sxs-lookup"><span data-stu-id="3a9d8-132">This is the number of days the logs are preserved in the storage account specified.</span></span> <span data-ttu-id="3a9d8-133">Aby zachować dane w nieskończoność, ustaw **wartość 0**.</span><span class="sxs-lookup"><span data-stu-id="3a9d8-133">To retain the data forever set this to **0**.</span></span> <span data-ttu-id="3a9d8-134">Jeśli nie jest określony, domyślnie przyjmowana jest **wartość 0**.</span><span class="sxs-lookup"><span data-stu-id="3a9d8-134">If it's not specified, then it defaults to **0**.</span></span> <span data-ttu-id="3a9d8-135">Do przechowywania danych będą stosowane zwykłe stawki za połączenia w standardowym magazynie lub w centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="3a9d8-135">Normal standard storage or event hub billing rates will apply for data retention.</span></span>

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

### <span data-ttu-id="3a9d8-136">-ServiceBusRuleId</span><span class="sxs-lookup"><span data-stu-id="3a9d8-136">-ServiceBusRuleId</span></span>
<span data-ttu-id="3a9d8-137">Określa identyfikator reguły magistrali usług.</span><span class="sxs-lookup"><span data-stu-id="3a9d8-137">Specifies the ID of the Service Bus rule.</span></span>

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

### <span data-ttu-id="3a9d8-138">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="3a9d8-138">-StorageAccountId</span></span>
<span data-ttu-id="3a9d8-139">Określa identyfikator konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="3a9d8-139">Specifies the ID of the Storage account.</span></span> <span data-ttu-id="3a9d8-140">Identyfikator to w pełni kwalifikowany identyfikator zasobów konta magazynu, na przykład</span><span class="sxs-lookup"><span data-stu-id="3a9d8-140">ID is the fully qualified Resource ID of the storage account for example</span></span>  

<span data-ttu-id="3a9d8-141">/subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount</span><span class="sxs-lookup"><span data-stu-id="3a9d8-141">/subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount</span></span>

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

### <span data-ttu-id="3a9d8-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a9d8-142">-DefaultProfile</span></span>
<span data-ttu-id="3a9d8-143">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3a9d8-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a9d8-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a9d8-144">CommonParameters</span></span>
<span data-ttu-id="3a9d8-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a9d8-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a9d8-146">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a9d8-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a9d8-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3a9d8-147">INPUTS</span></span>

## <span data-ttu-id="3a9d8-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3a9d8-148">OUTPUTS</span></span>

### <span data-ttu-id="3a9d8-149">Microsoft. Azure. Commands. Insights. OutputClasses. PSLogProfile</span><span class="sxs-lookup"><span data-stu-id="3a9d8-149">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile</span></span>

## <span data-ttu-id="3a9d8-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3a9d8-150">NOTES</span></span>

## <span data-ttu-id="3a9d8-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3a9d8-151">RELATED LINKS</span></span>

[<span data-ttu-id="3a9d8-152">Get-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="3a9d8-152">Get-AzureRmLogProfile</span></span>](./Get-AzureRmLogProfile.md)

[<span data-ttu-id="3a9d8-153">Remove-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="3a9d8-153">Remove-AzureRmLogProfile</span></span>](./Remove-AzureRmLogProfile.md)


