---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D927B159-AD68-4071-ADE3-FA2430750D72
online version: ''
schema: 2.0.0
ms.openlocfilehash: 001466cb00ad15f1cbfef6dcf9fd3ce9b931109b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055421"
---
# <span data-ttu-id="28824-101">Remove-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="28824-101">Remove-AzureStoreAddOn</span></span>

## <span data-ttu-id="28824-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="28824-102">SYNOPSIS</span></span>
<span data-ttu-id="28824-103">Usuwa istniejące wystąpienie dodatku.</span><span class="sxs-lookup"><span data-stu-id="28824-103">Removes an existing add-on instance.</span></span>

## <span data-ttu-id="28824-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="28824-104">SYNTAX</span></span>

```
Remove-AzureStoreAddOn -Name <String> [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="28824-105">Opis</span><span class="sxs-lookup"><span data-stu-id="28824-105">DESCRIPTION</span></span>
<span data-ttu-id="28824-106">W tym temacie opisano polecenie cmdlet w wersji 0.8.10 modułu PowerShell platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="28824-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="28824-107">Aby uzyskać wersję używanego modułu, należy wpisać w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="28824-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="28824-108">Usuwa istniejące wystąpienie dodatku z bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="28824-108">Removes an existing add-on instance from the current subscription.</span></span>

## <span data-ttu-id="28824-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="28824-109">EXAMPLES</span></span>

### <span data-ttu-id="28824-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="28824-110">Example 1</span></span>
```
PS C:\> Remove-AzureStoreAddOn MyAddOn
```

<span data-ttu-id="28824-111">W tym przykładzie usunięto dodatek o nazwie Moje oddodatek z bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="28824-111">This example removes an add-on named MyAddOn from the current subscription.</span></span>

## <span data-ttu-id="28824-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="28824-112">PARAMETERS</span></span>

### <span data-ttu-id="28824-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="28824-113">-Name</span></span>
<span data-ttu-id="28824-114">Określa nazwę wystąpienia dodatku, które ma zostać usunięte.</span><span class="sxs-lookup"><span data-stu-id="28824-114">Specifies the name of the add-on instance to remove.</span></span>

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

### <span data-ttu-id="28824-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="28824-115">-PassThru</span></span>
<span data-ttu-id="28824-116">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="28824-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="28824-117">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="28824-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="28824-118">-Profile</span><span class="sxs-lookup"><span data-stu-id="28824-118">-Profile</span></span>
<span data-ttu-id="28824-119">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="28824-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="28824-120">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="28824-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="28824-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28824-121">CommonParameters</span></span>
<span data-ttu-id="28824-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28824-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28824-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28824-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28824-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="28824-124">INPUTS</span></span>

## <span data-ttu-id="28824-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="28824-125">OUTPUTS</span></span>

## <span data-ttu-id="28824-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="28824-126">NOTES</span></span>

## <span data-ttu-id="28824-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="28824-127">RELATED LINKS</span></span>

[<span data-ttu-id="28824-128">Get-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="28824-128">Get-AzureStoreAddOn</span></span>](./Get-AzureStoreAddOn.md)

[<span data-ttu-id="28824-129">Nowe — AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="28824-129">New-AzureStoreAddOn</span></span>](./New-AzureStoreAddOn.md)

[<span data-ttu-id="28824-130">Set-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="28824-130">Set-AzureStoreAddOn</span></span>](./Set-AzureStoreAddOn.md)


