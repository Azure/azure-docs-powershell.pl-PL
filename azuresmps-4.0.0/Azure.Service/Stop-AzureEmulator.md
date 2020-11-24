---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 43E2C42E-16A3-426E-A7C4-33942F06F908
online version: ''
schema: 2.0.0
ms.openlocfilehash: 501a164fc4470a3d4fd6163050fba495ce3d2705
ms.sourcegitcommit: 25eca7b5f5480758aa2cd830458900cf91cf673c
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/24/2020
ms.locfileid: "95515096"
---
# <span data-ttu-id="cd260-101">Stop-AzureEmulator</span><span class="sxs-lookup"><span data-stu-id="cd260-101">Stop-AzureEmulator</span></span>

## <span data-ttu-id="cd260-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cd260-102">SYNOPSIS</span></span>
<span data-ttu-id="cd260-103">Zatrzymuje emulator obliczeniowy.</span><span class="sxs-lookup"><span data-stu-id="cd260-103">Stops the compute emulator.</span></span>

## <span data-ttu-id="cd260-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cd260-104">SYNTAX</span></span>

```
Stop-AzureEmulator [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="cd260-105">Opis</span><span class="sxs-lookup"><span data-stu-id="cd260-105">DESCRIPTION</span></span>
<span data-ttu-id="cd260-106">W tym temacie opisano polecenie cmdlet w wersji 0.8.10 modułu PowerShell platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="cd260-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="cd260-107">Aby uzyskać wersję używanego modułu, należy wpisać w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="cd260-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="cd260-108">Polecenie cmdlet **stop-AzureEmulator** zatrzymuje emulatora obliczeniowego platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="cd260-108">The **Stop-AzureEmulator** cmdlet stops the Azure Compute Emulator.</span></span>
<span data-ttu-id="cd260-109">Wszystkie usługi obecnie uruchomione w emulatorze zostaną usunięte.</span><span class="sxs-lookup"><span data-stu-id="cd260-109">Any services currently running in the emulator are removed.</span></span>

## <span data-ttu-id="cd260-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cd260-110">EXAMPLES</span></span>

## <span data-ttu-id="cd260-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cd260-111">PARAMETERS</span></span>

### <span data-ttu-id="cd260-112">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cd260-112">-PassThru</span></span>
<span data-ttu-id="cd260-113">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="cd260-113">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="cd260-114">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="cd260-114">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="cd260-115">-Profile</span><span class="sxs-lookup"><span data-stu-id="cd260-115">-Profile</span></span>
<span data-ttu-id="cd260-116">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd260-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="cd260-117">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="cd260-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="cd260-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd260-118">CommonParameters</span></span>
<span data-ttu-id="cd260-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd260-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd260-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd260-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd260-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cd260-121">INPUTS</span></span>

## <span data-ttu-id="cd260-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cd260-122">OUTPUTS</span></span>

## <span data-ttu-id="cd260-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cd260-123">NOTES</span></span>

## <span data-ttu-id="cd260-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cd260-124">RELATED LINKS</span></span>

[<span data-ttu-id="cd260-125">Start — AzureEmulator</span><span class="sxs-lookup"><span data-stu-id="cd260-125">Start-AzureEmulator</span></span>](./Start-AzureEmulator.md)


