---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 03E0442D-248E-41DB-98F5-DB3132CD0DCC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 492abdaab507b3ea5f7a8715c82dc0c29e3e94ef
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055278"
---
# <span data-ttu-id="0a2dd-101">Get-AzureSBLocation</span><span class="sxs-lookup"><span data-stu-id="0a2dd-101">Get-AzureSBLocation</span></span>

## <span data-ttu-id="0a2dd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0a2dd-102">SYNOPSIS</span></span>
<span data-ttu-id="0a2dd-103">Pobiera lokalizację magistrali usługowej.</span><span class="sxs-lookup"><span data-stu-id="0a2dd-103">Gets the location of the Service Bus.</span></span>

## <span data-ttu-id="0a2dd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0a2dd-104">SYNTAX</span></span>

```
Get-AzureSBLocation [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="0a2dd-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0a2dd-105">DESCRIPTION</span></span>
<span data-ttu-id="0a2dd-106">W tym temacie opisano polecenie cmdlet w wersji 0.8.10 modułu PowerShell platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="0a2dd-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="0a2dd-107">Aby uzyskać wersję używanego modułu, należy wpisać w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="0a2dd-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="0a2dd-108">Polecenie cmdlet **Get-AzureSBLocation** zwraca lokalizacje, z których usługa Service Bus jest dostępna.</span><span class="sxs-lookup"><span data-stu-id="0a2dd-108">The **Get-AzureSBLocation** cmdlet returns the locations from which the Service Bus is available.</span></span>

[!INCLUDE [sb-deprecation.md](../include/sb-deprecation.md)]

## <span data-ttu-id="0a2dd-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0a2dd-109">EXAMPLES</span></span>

### <span data-ttu-id="0a2dd-110">Przykład 1: Uzyskiwanie lokalizacji usługi Service Bus</span><span class="sxs-lookup"><span data-stu-id="0a2dd-110">Example 1: Get the Service Bus location</span></span>
```
PS C:\> Get-AzureSBLocation
```

<span data-ttu-id="0a2dd-111">W tym przykładzie jest pobierana lokalizacja magistrali usług.</span><span class="sxs-lookup"><span data-stu-id="0a2dd-111">This example gets the location of the Service Bus.</span></span>

## <span data-ttu-id="0a2dd-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0a2dd-112">PARAMETERS</span></span>

### <span data-ttu-id="0a2dd-113">-Profile</span><span class="sxs-lookup"><span data-stu-id="0a2dd-113">-Profile</span></span>
<span data-ttu-id="0a2dd-114">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0a2dd-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0a2dd-115">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="0a2dd-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0a2dd-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a2dd-116">CommonParameters</span></span>
<span data-ttu-id="0a2dd-117">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a2dd-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a2dd-118">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a2dd-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a2dd-119">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0a2dd-119">INPUTS</span></span>

## <span data-ttu-id="0a2dd-120">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0a2dd-120">OUTPUTS</span></span>

## <span data-ttu-id="0a2dd-121">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0a2dd-121">NOTES</span></span>

## <span data-ttu-id="0a2dd-122">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0a2dd-122">RELATED LINKS</span></span>

[<span data-ttu-id="0a2dd-123">Get-AzureSBNamespace</span><span class="sxs-lookup"><span data-stu-id="0a2dd-123">Get-AzureSBNamespace</span></span>](./Get-AzureSBNamespace.md)


