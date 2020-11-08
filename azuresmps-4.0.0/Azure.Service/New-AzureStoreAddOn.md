---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 793037C4-8FE5-4799-B59B-94C1605D9F4E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 593ea36e90635472db1f8568254657f782bd1200
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055167"
---
# <span data-ttu-id="99bdc-101">New-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="99bdc-101">New-AzureStoreAddOn</span></span>

## <span data-ttu-id="99bdc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="99bdc-102">SYNOPSIS</span></span>
<span data-ttu-id="99bdc-103">Kupując nowe wystąpienie dodatku.</span><span class="sxs-lookup"><span data-stu-id="99bdc-103">Buys a new add-on instance.</span></span>

## <span data-ttu-id="99bdc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="99bdc-104">SYNTAX</span></span>

```
New-AzureStoreAddOn -Name <String> -AddOn <String> -Plan <String> -Location <String> [-PromotionCode <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="99bdc-105">Opis</span><span class="sxs-lookup"><span data-stu-id="99bdc-105">DESCRIPTION</span></span>
<span data-ttu-id="99bdc-106">W tym temacie opisano polecenie cmdlet w wersji 0.8.10 modułu PowerShell platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="99bdc-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="99bdc-107">Aby uzyskać wersję używanego modułu, należy wpisać w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="99bdc-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="99bdc-108">Kupując nowe wystąpienie dodatku ze Sklepu Azure.</span><span class="sxs-lookup"><span data-stu-id="99bdc-108">Buys a new add-on instance from the Azure Store.</span></span>

## <span data-ttu-id="99bdc-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="99bdc-109">EXAMPLES</span></span>

### <span data-ttu-id="99bdc-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="99bdc-110">Example 1</span></span>
```
PS C:\> New-AzureStoreAddOn -Name MyAddOn -AddOn AddonId -Plan PlanId -Location "West US"
```

<span data-ttu-id="99bdc-111">W tym przykładzie zakupowano dodatek o nazwie Moje PlanId w zachodniej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="99bdc-111">This example buys an add-on named MyAddOn with a PlanId in West US location.</span></span>

### <span data-ttu-id="99bdc-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="99bdc-112">Example 2</span></span>
```
PS C:\> New-AzureStoreAddOn -Name MyAddOn -AddOn AddonId -Plan PlanId -Location "West US" -PromotionCode MyPromoCode
```

<span data-ttu-id="99bdc-113">W tym przykładzie użyto kodu promocyjnego do zakupu dodatku.</span><span class="sxs-lookup"><span data-stu-id="99bdc-113">This example uses a promotional code to buy an add-on.</span></span>

## <span data-ttu-id="99bdc-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="99bdc-114">PARAMETERS</span></span>

### <span data-ttu-id="99bdc-115">-Dodatek</span><span class="sxs-lookup"><span data-stu-id="99bdc-115">-AddOn</span></span>
<span data-ttu-id="99bdc-116">Określa identyfikator dodatku.</span><span class="sxs-lookup"><span data-stu-id="99bdc-116">Specifies the add-on ID.</span></span>

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

### <span data-ttu-id="99bdc-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="99bdc-117">-Location</span></span>
<span data-ttu-id="99bdc-118">Określa lokalizację wystąpienia dodatku.</span><span class="sxs-lookup"><span data-stu-id="99bdc-118">Specifies the add-on instance location.</span></span>

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

### <span data-ttu-id="99bdc-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="99bdc-119">-Name</span></span>
<span data-ttu-id="99bdc-120">Określa nazwę wystąpienia dodatku.</span><span class="sxs-lookup"><span data-stu-id="99bdc-120">Specifies the name of the add-on instance.</span></span>

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

### <span data-ttu-id="99bdc-121">-Plan</span><span class="sxs-lookup"><span data-stu-id="99bdc-121">-Plan</span></span>
<span data-ttu-id="99bdc-122">Określa identyfikator planu.</span><span class="sxs-lookup"><span data-stu-id="99bdc-122">Specifies the plan ID.</span></span>

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

### <span data-ttu-id="99bdc-123">-Profile</span><span class="sxs-lookup"><span data-stu-id="99bdc-123">-Profile</span></span>
<span data-ttu-id="99bdc-124">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="99bdc-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="99bdc-125">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="99bdc-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99bdc-126">-PromotionCode</span><span class="sxs-lookup"><span data-stu-id="99bdc-126">-PromotionCode</span></span>
<span data-ttu-id="99bdc-127">Umożliwia określenie kodu promocyjnego, który ma zostać zastosowany do zakupu.</span><span class="sxs-lookup"><span data-stu-id="99bdc-127">Specifies a promotion code to apply to the purchase.</span></span>

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

### <span data-ttu-id="99bdc-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99bdc-128">CommonParameters</span></span>
<span data-ttu-id="99bdc-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99bdc-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99bdc-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99bdc-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99bdc-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="99bdc-131">INPUTS</span></span>

## <span data-ttu-id="99bdc-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="99bdc-132">OUTPUTS</span></span>

## <span data-ttu-id="99bdc-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="99bdc-133">NOTES</span></span>

## <span data-ttu-id="99bdc-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="99bdc-134">RELATED LINKS</span></span>

[<span data-ttu-id="99bdc-135">Get-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="99bdc-135">Get-AzureStoreAddOn</span></span>](./Get-AzureStoreAddOn.md)

[<span data-ttu-id="99bdc-136">Remove-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="99bdc-136">Remove-AzureStoreAddOn</span></span>](./Remove-AzureStoreAddOn.md)

[<span data-ttu-id="99bdc-137">Set-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="99bdc-137">Set-AzureStoreAddOn</span></span>](./Set-AzureStoreAddOn.md)


