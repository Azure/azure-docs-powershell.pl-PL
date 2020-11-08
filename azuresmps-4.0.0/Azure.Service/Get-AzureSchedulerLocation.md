---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 410A58A3-CB0E-43FE-B490-B1520BD1CCEC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4c445e2b42738f288de960f30f4c98d909c71784
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054577"
---
# <span data-ttu-id="a1fd1-101">Get-AzureSchedulerLocation</span><span class="sxs-lookup"><span data-stu-id="a1fd1-101">Get-AzureSchedulerLocation</span></span>

## <span data-ttu-id="a1fd1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a1fd1-102">SYNOPSIS</span></span>
<span data-ttu-id="a1fd1-103">Pobiera dostępne lokalizacje harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="a1fd1-103">Gets available scheduler locations.</span></span>

## <span data-ttu-id="a1fd1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a1fd1-104">SYNTAX</span></span>

```
Get-AzureSchedulerLocation [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="a1fd1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a1fd1-105">DESCRIPTION</span></span>
<span data-ttu-id="a1fd1-106">W tym temacie opisano polecenie cmdlet w wersji 0.8.10 modułu PowerShell platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="a1fd1-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="a1fd1-107">Aby uzyskać wersję używanego modułu, należy wpisać w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="a1fd1-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="a1fd1-108">Polecenie cmdlet **Get-AzureSchedulerLocation** Pobiera dostępne lokalizacje harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="a1fd1-108">The **Get-AzureSchedulerLocation** cmdlet gets available scheduler locations.</span></span>

## <span data-ttu-id="a1fd1-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a1fd1-109">EXAMPLES</span></span>

### <span data-ttu-id="a1fd1-110">Przykład 1: uzyskiwanie dostępnych lokalizacji harmonogramu</span><span class="sxs-lookup"><span data-stu-id="a1fd1-110">Example 1: Get available scheduler locations</span></span>
```
PS C:\> Get-AzureSchedulerLocation
```

<span data-ttu-id="a1fd1-111">To polecenie pobiera dostępne lokalizacje harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="a1fd1-111">This command gets available scheduler locations.</span></span>

## <span data-ttu-id="a1fd1-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a1fd1-112">PARAMETERS</span></span>

### <span data-ttu-id="a1fd1-113">-Profile</span><span class="sxs-lookup"><span data-stu-id="a1fd1-113">-Profile</span></span>
<span data-ttu-id="a1fd1-114">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a1fd1-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a1fd1-115">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="a1fd1-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a1fd1-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1fd1-116">CommonParameters</span></span>
<span data-ttu-id="a1fd1-117">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1fd1-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1fd1-118">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1fd1-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1fd1-119">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a1fd1-119">INPUTS</span></span>

## <span data-ttu-id="a1fd1-120">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a1fd1-120">OUTPUTS</span></span>

## <span data-ttu-id="a1fd1-121">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a1fd1-121">NOTES</span></span>

## <span data-ttu-id="a1fd1-122">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a1fd1-122">RELATED LINKS</span></span>

[<span data-ttu-id="a1fd1-123">Get-AzureSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="a1fd1-123">Get-AzureSchedulerJob</span></span>](./Get-AzureSchedulerJob.md)

[<span data-ttu-id="a1fd1-124">Get-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="a1fd1-124">Get-AzureSchedulerJobCollection</span></span>](./Get-AzureSchedulerJobCollection.md)

[<span data-ttu-id="a1fd1-125">Get-AzureSchedulerJobHistory</span><span class="sxs-lookup"><span data-stu-id="a1fd1-125">Get-AzureSchedulerJobHistory</span></span>](./Get-AzureSchedulerJobHistory.md)


