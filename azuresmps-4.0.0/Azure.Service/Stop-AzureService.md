---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 939A28A4-394A-4447-9EFA-8F2876D04DCD
online version: ''
schema: 2.0.0
ms.openlocfilehash: b140c2c0efac81e361e2bab510cfeaf6210ef884
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054773"
---
# <span data-ttu-id="73a72-101">Stop-AzureService</span><span class="sxs-lookup"><span data-stu-id="73a72-101">Stop-AzureService</span></span>

## <span data-ttu-id="73a72-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="73a72-102">SYNOPSIS</span></span>
<span data-ttu-id="73a72-103">Zatrzymuje bieżącą usługę hostowaną.</span><span class="sxs-lookup"><span data-stu-id="73a72-103">Stops the current hosted service.</span></span>

## <span data-ttu-id="73a72-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="73a72-104">SYNTAX</span></span>

```
Stop-AzureService [-ServiceName <String>] [-Slot <String>] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="73a72-105">Opis</span><span class="sxs-lookup"><span data-stu-id="73a72-105">DESCRIPTION</span></span>
<span data-ttu-id="73a72-106">W tym temacie opisano polecenie cmdlet w wersji 0.8.10 modułu PowerShell platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="73a72-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="73a72-107">Aby uzyskać wersję używanego modułu, należy wpisać w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="73a72-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="73a72-108">Polecenie cmdlet **stop-AzureService** zatrzymuje bieżącą usługę hostowaną w określonym gnieździe w systemie Windows Azure.</span><span class="sxs-lookup"><span data-stu-id="73a72-108">The **Stop-AzureService** cmdlet stops the current hosted service in the specified slot in Windows Azure.</span></span>
<span data-ttu-id="73a72-109">Jeśli nie określono żadnego miejsca, polecenie cmdlet zatrzymuje usługę w gnieździe produkcyjnym.</span><span class="sxs-lookup"><span data-stu-id="73a72-109">If no slot is specified, the cmdlet stops the service in the Production slot.</span></span>

## <span data-ttu-id="73a72-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="73a72-110">EXAMPLES</span></span>

## <span data-ttu-id="73a72-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="73a72-111">PARAMETERS</span></span>

### <span data-ttu-id="73a72-112">-PassThru</span><span class="sxs-lookup"><span data-stu-id="73a72-112">-PassThru</span></span>
<span data-ttu-id="73a72-113">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="73a72-113">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="73a72-114">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="73a72-114">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73a72-115">-Profile</span><span class="sxs-lookup"><span data-stu-id="73a72-115">-Profile</span></span>
<span data-ttu-id="73a72-116">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="73a72-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="73a72-117">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="73a72-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="73a72-118">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="73a72-118">-ServiceName</span></span>
<span data-ttu-id="73a72-119">Określa nazwę hostowanej usługi do zatrzymania.</span><span class="sxs-lookup"><span data-stu-id="73a72-119">Specifies the name of the hosted service to stop.</span></span>
<span data-ttu-id="73a72-120">Jeśli nie podano nazwy, polecenie cmdlet zatrzymuje bieżącą usługę hostowaną.</span><span class="sxs-lookup"><span data-stu-id="73a72-120">If no name is specified, the cmdlet stops the current hosted service.</span></span>

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

### <span data-ttu-id="73a72-121">-Slot</span><span class="sxs-lookup"><span data-stu-id="73a72-121">-Slot</span></span>
<span data-ttu-id="73a72-122">Określa miejsce, w którym usługa jest hostowana, czyli przemieszczanie lub tworzenie.</span><span class="sxs-lookup"><span data-stu-id="73a72-122">Specifies the slot where the service is hosted, either Staging or Production.</span></span>
<span data-ttu-id="73a72-123">Jeśli nie określono żadnego gniazda, przyjmowana jest produkcja.</span><span class="sxs-lookup"><span data-stu-id="73a72-123">If no slot is specified,  Production is assumed.</span></span>

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

### <span data-ttu-id="73a72-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73a72-124">CommonParameters</span></span>
<span data-ttu-id="73a72-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73a72-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73a72-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73a72-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73a72-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="73a72-127">INPUTS</span></span>

## <span data-ttu-id="73a72-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="73a72-128">OUTPUTS</span></span>

## <span data-ttu-id="73a72-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="73a72-129">NOTES</span></span>

## <span data-ttu-id="73a72-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="73a72-130">RELATED LINKS</span></span>

[<span data-ttu-id="73a72-131">Remove-AzureService</span><span class="sxs-lookup"><span data-stu-id="73a72-131">Remove-AzureService</span></span>](./Remove-AzureService.md)

[<span data-ttu-id="73a72-132">Start — AzureService</span><span class="sxs-lookup"><span data-stu-id="73a72-132">Start-AzureService</span></span>](./Start-AzureService.md)


