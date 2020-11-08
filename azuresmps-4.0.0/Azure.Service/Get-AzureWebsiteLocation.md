---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 6313BAB9-32D1-4B4B-A0C7-345F20629505
online version: ''
schema: 2.0.0
ms.openlocfilehash: 73b461bb5dfd70576079d333366c50f5e6f56900
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055238"
---
# <span data-ttu-id="e6ea4-101">Get-AzureWebsiteLocation</span><span class="sxs-lookup"><span data-stu-id="e6ea4-101">Get-AzureWebsiteLocation</span></span>

## <span data-ttu-id="e6ea4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e6ea4-102">SYNOPSIS</span></span>
<span data-ttu-id="e6ea4-103">Pobiera wszystkie dostępne lokalizacje witryn internetowych.</span><span class="sxs-lookup"><span data-stu-id="e6ea4-103">Gets all available website locations.</span></span>

## <span data-ttu-id="e6ea4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e6ea4-104">SYNTAX</span></span>

```
Get-AzureWebsiteLocation [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e6ea4-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e6ea4-105">DESCRIPTION</span></span>
<span data-ttu-id="e6ea4-106">W tym temacie opisano polecenie cmdlet w wersji 0.8.10 modułu PowerShell platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="e6ea4-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="e6ea4-107">Aby uzyskać wersję używanego modułu, należy wpisać w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="e6ea4-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="e6ea4-108">Pobiera wszystkie dostępne lokalizacje witryn internetowych dla bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="e6ea4-108">Gets all of the available website locations for the current subscription</span></span>

## <span data-ttu-id="e6ea4-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e6ea4-109">EXAMPLES</span></span>

### <span data-ttu-id="e6ea4-110">Przykład 1: pobieranie wszystkich dostępnych lokalizacji</span><span class="sxs-lookup"><span data-stu-id="e6ea4-110">Example 1: Get all available locations</span></span>
```
PS C:\> Get-AzureWebsiteLocations
```

<span data-ttu-id="e6ea4-111">W tym przykładzie są pobierane wszystkie dostępne lokalizacje witryn internetowych dla bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="e6ea4-111">This example gets all of the available website locations for the current subscription.</span></span>

## <span data-ttu-id="e6ea4-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e6ea4-112">PARAMETERS</span></span>

### <span data-ttu-id="e6ea4-113">-Profile</span><span class="sxs-lookup"><span data-stu-id="e6ea4-113">-Profile</span></span>
<span data-ttu-id="e6ea4-114">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e6ea4-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e6ea4-115">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="e6ea4-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e6ea4-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6ea4-116">CommonParameters</span></span>
<span data-ttu-id="e6ea4-117">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6ea4-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6ea4-118">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6ea4-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6ea4-119">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e6ea4-119">INPUTS</span></span>

## <span data-ttu-id="e6ea4-120">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e6ea4-120">OUTPUTS</span></span>

## <span data-ttu-id="e6ea4-121">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e6ea4-121">NOTES</span></span>

## <span data-ttu-id="e6ea4-122">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e6ea4-122">RELATED LINKS</span></span>

[<span data-ttu-id="e6ea4-123">Nowe — AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="e6ea4-123">New-AzureWebsite</span></span>](./New-AzureWebsite.md)


