---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: F5EC8E00-E504-436A-96FF-4E886579AEA4
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5b72fcfac0b000a8fcfc11dbab6961460cb25b8b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055381"
---
# <span data-ttu-id="3e511-101">Set-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="3e511-101">Set-AzureStoreAddOn</span></span>

## <span data-ttu-id="3e511-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3e511-102">SYNOPSIS</span></span>
<span data-ttu-id="3e511-103">Aktualizuje istniejące wystąpienie dodatku.</span><span class="sxs-lookup"><span data-stu-id="3e511-103">Updates an existing add-on instance.</span></span>

## <span data-ttu-id="3e511-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3e511-104">SYNTAX</span></span>

```
Set-AzureStoreAddOn -Name <String> -Plan <String> [-PromotionCode <String>] [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3e511-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3e511-105">DESCRIPTION</span></span>
<span data-ttu-id="3e511-106">W tym temacie opisano polecenie cmdlet w wersji 0.8.10 modułu PowerShell platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3e511-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="3e511-107">Aby uzyskać wersję używanego modułu, należy wpisać w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="3e511-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="3e511-108">To polecenie cmdlet umożliwia zaktualizowanie istniejącego wystąpienia dodatku na podstawie bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="3e511-108">This cmdlet updates an existing add-on instance from the current subscription.</span></span>

## <span data-ttu-id="3e511-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3e511-109">EXAMPLES</span></span>

### <span data-ttu-id="3e511-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3e511-110">Example 1</span></span>
```
PS C:\> Set-AzureStoreAddOn MyAddOn NewPlanId
```

<span data-ttu-id="3e511-111">W tym przykładzie jest aktualizowana dodatek o nowym IDENTYFIKATORze planu.</span><span class="sxs-lookup"><span data-stu-id="3e511-111">This example updates an add-on with a new plan ID.</span></span>

### <span data-ttu-id="3e511-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="3e511-112">Example 2</span></span>
```
PS C:\> Set-AzureStoreAddOn MyAddOn NewPlanId MyPromoCode
```

<span data-ttu-id="3e511-113">W tym przykładzie Zaktualizowano dodatek przy użyciu nowego identyfikatora planu i kodu promocyjnego.</span><span class="sxs-lookup"><span data-stu-id="3e511-113">This example updates an add-on with a new plan ID and promotional code.</span></span>

## <span data-ttu-id="3e511-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3e511-114">PARAMETERS</span></span>

### <span data-ttu-id="3e511-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3e511-115">-Name</span></span>
<span data-ttu-id="3e511-116">Określa nazwę wystąpienia dodatku.</span><span class="sxs-lookup"><span data-stu-id="3e511-116">Specifies the name of the add-on instance.</span></span>

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

### <span data-ttu-id="3e511-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3e511-117">-PassThru</span></span>
<span data-ttu-id="3e511-118">Jeśli ta funkcja jest określona, polecenie cmdlet zwraca wartość PRAWDA, jeśli wykonanie polecenia zakończy się niepowodzeniem i FAŁSZ.</span><span class="sxs-lookup"><span data-stu-id="3e511-118">If specified, the cmdlet returns true if the command succeeds and false if it fails.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e511-119">-Plan</span><span class="sxs-lookup"><span data-stu-id="3e511-119">-Plan</span></span>
<span data-ttu-id="3e511-120">Określa identyfikator planu.</span><span class="sxs-lookup"><span data-stu-id="3e511-120">Specifies the plan ID.</span></span>

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

### <span data-ttu-id="3e511-121">-Profile</span><span class="sxs-lookup"><span data-stu-id="3e511-121">-Profile</span></span>
<span data-ttu-id="3e511-122">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e511-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3e511-123">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="3e511-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3e511-124">-PromotionCode</span><span class="sxs-lookup"><span data-stu-id="3e511-124">-PromotionCode</span></span>
<span data-ttu-id="3e511-125">Określa kod promocyjny.</span><span class="sxs-lookup"><span data-stu-id="3e511-125">Specifies the promotional code.</span></span>

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

### <span data-ttu-id="3e511-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e511-126">CommonParameters</span></span>
<span data-ttu-id="3e511-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e511-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e511-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e511-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e511-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3e511-129">INPUTS</span></span>

## <span data-ttu-id="3e511-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3e511-130">OUTPUTS</span></span>

## <span data-ttu-id="3e511-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3e511-131">NOTES</span></span>

## <span data-ttu-id="3e511-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3e511-132">RELATED LINKS</span></span>

[<span data-ttu-id="3e511-133">Get-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="3e511-133">Get-AzureStoreAddOn</span></span>](./Get-AzureStoreAddOn.md)

[<span data-ttu-id="3e511-134">Nowe — AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="3e511-134">New-AzureStoreAddOn</span></span>](./New-AzureStoreAddOn.md)

[<span data-ttu-id="3e511-135">Remove-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="3e511-135">Remove-AzureStoreAddOn</span></span>](./Remove-AzureStoreAddOn.md)


