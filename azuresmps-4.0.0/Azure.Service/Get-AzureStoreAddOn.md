---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 61CF7F95-F0BB-4282-A971-537CB73708B1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3d5774213054f3e9e56e9804a9319e31f095f868
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054513"
---
# <span data-ttu-id="318b2-101">Get-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="318b2-101">Get-AzureStoreAddOn</span></span>

## <span data-ttu-id="318b2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="318b2-102">SYNOPSIS</span></span>
<span data-ttu-id="318b2-103">Pobiera dostępne dodatki ze Sklepu Azure.</span><span class="sxs-lookup"><span data-stu-id="318b2-103">Gets the available Azure Store add-ons.</span></span>

## <span data-ttu-id="318b2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="318b2-104">SYNTAX</span></span>

### <span data-ttu-id="318b2-105">ListAvailable</span><span class="sxs-lookup"><span data-stu-id="318b2-105">ListAvailable</span></span>
```
Get-AzureStoreAddOn [-ListAvailable] [-Country <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="318b2-106">Getdodatków</span><span class="sxs-lookup"><span data-stu-id="318b2-106">GetAddOn</span></span>
```
Get-AzureStoreAddOn [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="318b2-107">Opis</span><span class="sxs-lookup"><span data-stu-id="318b2-107">DESCRIPTION</span></span>
<span data-ttu-id="318b2-108">W tym temacie opisano polecenie cmdlet w wersji 0.8.10 modułu PowerShell platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="318b2-108">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="318b2-109">Aby uzyskać wersję używanego modułu, należy wpisać w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="318b2-109">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="318b2-110">Pobiera wszystkie dostępne dodatki na potrzeby zakupu ze Sklepu Azure Store lub pobiera istniejące wystąpienia dodatków dla bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="318b2-110">Gets all the available add-ons for purchasing from the Azure Store, or gets the existing add-on instances for the current subscription.</span></span>

## <span data-ttu-id="318b2-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="318b2-111">EXAMPLES</span></span>

### <span data-ttu-id="318b2-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="318b2-112">Example 1</span></span>
```
PS C:\> Get-AzureStoreAddOn
```

<span data-ttu-id="318b2-113">W tym przykładzie są pobierane wszystkie zakupione wystąpienia dodatków dla bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="318b2-113">This example gets all purchased add-on instances for the current subscription.</span></span>

### <span data-ttu-id="318b2-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="318b2-114">Example 2</span></span>
```
PS C:\> Get-AzureStoreAddOn -ListAvailable
```

<span data-ttu-id="318b2-115">W tym przykładzie są pobierane wszystkie dostępne dodatki dotyczące zakupu w Stanach Zjednoczonych ze Sklepu Azure.</span><span class="sxs-lookup"><span data-stu-id="318b2-115">This example gets all the available add-ons for purchasing in United States from the Azure Store.</span></span>

### <span data-ttu-id="318b2-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="318b2-116">Example 3</span></span>
```
PS C:\> Get-AzureStoreAddOn -Name MyAddOn
```

<span data-ttu-id="318b2-117">W tym przykładzie jest pobierany dodatek o nazwie Moje oddodatek z zakupionego wystąpienia dodatku w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="318b2-117">This example gets an add-on named MyAddOn from the purchased add-on instance in the current subscription.</span></span>

## <span data-ttu-id="318b2-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="318b2-118">PARAMETERS</span></span>

### <span data-ttu-id="318b2-119">-Country</span><span class="sxs-lookup"><span data-stu-id="318b2-119">-Country</span></span>
<span data-ttu-id="318b2-120">Jeśli ta funkcja jest określona, zwraca tylko wystąpienia dodatków ze Sklepu Azure dostępne w określonym kraju.</span><span class="sxs-lookup"><span data-stu-id="318b2-120">If specified, returns only the Azure Store add-on instances available in the specified country.</span></span>
<span data-ttu-id="318b2-121">Wartość domyślna to "my".</span><span class="sxs-lookup"><span data-stu-id="318b2-121">The default is "US".</span></span>

```yaml
Type: String
Parameter Sets: ListAvailable
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="318b2-122">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="318b2-122">-ListAvailable</span></span>
<span data-ttu-id="318b2-123">Jeśli ta usługa jest określona, pobieraj dostępne dodatki do zakupu w Sklepie Azure.</span><span class="sxs-lookup"><span data-stu-id="318b2-123">If specified, gets available add-ons for purchasing from the Azure Store.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ListAvailable
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="318b2-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="318b2-124">-Name</span></span>
<span data-ttu-id="318b2-125">Zwraca dodatek zgodny z określoną nazwą.</span><span class="sxs-lookup"><span data-stu-id="318b2-125">Returns the add-on that matches the specified name.</span></span>

```yaml
Type: String
Parameter Sets: GetAddOn
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="318b2-126">-Profile</span><span class="sxs-lookup"><span data-stu-id="318b2-126">-Profile</span></span>
<span data-ttu-id="318b2-127">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="318b2-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="318b2-128">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="318b2-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="318b2-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="318b2-129">CommonParameters</span></span>
<span data-ttu-id="318b2-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="318b2-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="318b2-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="318b2-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="318b2-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="318b2-132">INPUTS</span></span>

## <span data-ttu-id="318b2-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="318b2-133">OUTPUTS</span></span>

## <span data-ttu-id="318b2-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="318b2-134">NOTES</span></span>

## <span data-ttu-id="318b2-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="318b2-135">RELATED LINKS</span></span>

[<span data-ttu-id="318b2-136">Nowe — AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="318b2-136">New-AzureStoreAddOn</span></span>](./New-AzureStoreAddOn.md)

[<span data-ttu-id="318b2-137">Remove-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="318b2-137">Remove-AzureStoreAddOn</span></span>](./Remove-AzureStoreAddOn.md)

[<span data-ttu-id="318b2-138">Set-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="318b2-138">Set-AzureStoreAddOn</span></span>](./Set-AzureStoreAddOn.md)


