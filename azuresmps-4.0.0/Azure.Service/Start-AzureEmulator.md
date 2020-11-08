---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: A1815E7F-720E-4526-A779-106C181B840D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 22b04496d9ce310b58662c62b70a195e8cfa8878
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054997"
---
# <span data-ttu-id="d2828-101">Start-AzureEmulator</span><span class="sxs-lookup"><span data-stu-id="d2828-101">Start-AzureEmulator</span></span>

## <span data-ttu-id="d2828-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d2828-102">SYNOPSIS</span></span>
<span data-ttu-id="d2828-103">Uruchamia emulatory obliczeniowe i magazynowe.</span><span class="sxs-lookup"><span data-stu-id="d2828-103">Starts the compute and storage emulators.</span></span>

## <span data-ttu-id="d2828-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d2828-104">SYNTAX</span></span>

```
Start-AzureEmulator [-Launch] [-Mode <ComputeEmulatorMode>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d2828-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d2828-105">DESCRIPTION</span></span>
<span data-ttu-id="d2828-106">W tym temacie opisano polecenie cmdlet w wersji 0.8.10 modułu PowerShell platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d2828-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="d2828-107">Aby uzyskać wersję używanego modułu, należy wpisać w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="d2828-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="d2828-108">Polecenie cmdlet **Start-AzureEmulator** uruchamia zarówno emulatory obliczeniowe, jak i magazynowe oraz hostuje bieżącą usługę w emulatorze obliczeniowym.</span><span class="sxs-lookup"><span data-stu-id="d2828-108">The **Start-AzureEmulator** cmdlet starts both the compute and storage emulators and hosts the current service in the compute emulator.</span></span>

## <span data-ttu-id="d2828-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d2828-109">EXAMPLES</span></span>

### <span data-ttu-id="d2828-110">Przykład 1. Uruchom emulator i uruchom przeglądarkę</span><span class="sxs-lookup"><span data-stu-id="d2828-110">Example 1: Start the emulator and launch a browser</span></span>
```
PS C:\> Start-AzureEmulator -L
```

<span data-ttu-id="d2828-111">W tym przykładzie usługa jest uruchamiana w emulatorze Azure i uruchamia nowe okno przeglądarki w emulowanej usłudze.</span><span class="sxs-lookup"><span data-stu-id="d2828-111">This example runs the service in the Azure emulator and launches a new browser window on the emulated service.</span></span>

## <span data-ttu-id="d2828-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d2828-112">PARAMETERS</span></span>

### <span data-ttu-id="d2828-113">-Uruchom</span><span class="sxs-lookup"><span data-stu-id="d2828-113">-Launch</span></span>
<span data-ttu-id="d2828-114">Otwiera nowe okno przeglądarki w usłudze po jej umieszczeniu w emulatorze.</span><span class="sxs-lookup"><span data-stu-id="d2828-114">Opens a new browser window on the service after hosting it in the emulator.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: ln

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2828-115">-Mode (tryb)</span><span class="sxs-lookup"><span data-stu-id="d2828-115">-Mode</span></span>
<span data-ttu-id="d2828-116">Określa tryb emulatora.</span><span class="sxs-lookup"><span data-stu-id="d2828-116">Specifies the emulator mode.</span></span>
<span data-ttu-id="d2828-117">Prawidłowe wartości to: Full i Express.</span><span class="sxs-lookup"><span data-stu-id="d2828-117">Valid values are: Full and Express.</span></span>
<span data-ttu-id="d2828-118">Wartość domyślna to ekspresowa.</span><span class="sxs-lookup"><span data-stu-id="d2828-118">The default value is Express.</span></span>

```yaml
Type: ComputeEmulatorMode
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2828-119">-Profile</span><span class="sxs-lookup"><span data-stu-id="d2828-119">-Profile</span></span>
<span data-ttu-id="d2828-120">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2828-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d2828-121">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="d2828-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d2828-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2828-122">CommonParameters</span></span>
<span data-ttu-id="d2828-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2828-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2828-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2828-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2828-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d2828-125">INPUTS</span></span>

## <span data-ttu-id="d2828-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d2828-126">OUTPUTS</span></span>

## <span data-ttu-id="d2828-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d2828-127">NOTES</span></span>

## <span data-ttu-id="d2828-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d2828-128">RELATED LINKS</span></span>

[<span data-ttu-id="d2828-129">Nowe — AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="d2828-129">New-AzureServiceProject</span></span>](./New-AzureServiceProject.md)

[<span data-ttu-id="d2828-130">Publikowanie — AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="d2828-130">Publish-AzureServiceProject</span></span>](./Publish-AzureServiceProject.md)

[<span data-ttu-id="d2828-131">Zatrzymaj — AzureEmulator</span><span class="sxs-lookup"><span data-stu-id="d2828-131">Stop-AzureEmulator</span></span>](./Stop-AzureEmulator.md)


