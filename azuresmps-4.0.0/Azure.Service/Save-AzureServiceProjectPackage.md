---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 9445B7FA-FC72-4F71-BD44-8AA55BE9BA0E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1d2a3dbabb5bbe78ed571806aa69b9d79d4782b3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054426"
---
# <span data-ttu-id="b1da4-101">Save-AzureServiceProjectPackage</span><span class="sxs-lookup"><span data-stu-id="b1da4-101">Save-AzureServiceProjectPackage</span></span>

## <span data-ttu-id="b1da4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b1da4-102">SYNOPSIS</span></span>
<span data-ttu-id="b1da4-103">Pakuj projekt usługi na pakiet usługi Azure Cloud.</span><span class="sxs-lookup"><span data-stu-id="b1da4-103">Packages the service project into Azure cloud package.</span></span>

## <span data-ttu-id="b1da4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b1da4-104">SYNTAX</span></span>

```
Save-AzureServiceProjectPackage [-Local] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b1da4-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b1da4-105">DESCRIPTION</span></span>
<span data-ttu-id="b1da4-106">W tym temacie opisano polecenie cmdlet w wersji 0.8.10 modułu PowerShell platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b1da4-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="b1da4-107">Aby uzyskać wersję używanego modułu, należy wpisać w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="b1da4-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="b1da4-108">Polecenie cmdlet **Save-AzureServiceProjectPackage** umożliwia pakowanie projektu usługi w usłudze Azure Cloud (\*. cspkg).</span><span class="sxs-lookup"><span data-stu-id="b1da4-108">The **Save-AzureServiceProjectPackage** cmdlet packages the service project into an Azure cloud package (\*.cspkg).</span></span>

## <span data-ttu-id="b1da4-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b1da4-109">EXAMPLES</span></span>

### <span data-ttu-id="b1da4-110">Przykład 1. Tworzenie pakietu projektu usługi</span><span class="sxs-lookup"><span data-stu-id="b1da4-110">Example 1: Create a service project package</span></span>
```
PS C:\> Save-AzureServiceProjectPackage
```

<span data-ttu-id="b1da4-111">W tym przykładzie przedstawiono tworzenie pliku \*. cspgk dla projektu usługi o nazwie MyAzureServiceProject.</span><span class="sxs-lookup"><span data-stu-id="b1da4-111">This example creates a \*.cspgk for a service project named MyAzureServiceProject.</span></span>

## <span data-ttu-id="b1da4-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b1da4-112">PARAMETERS</span></span>

### <span data-ttu-id="b1da4-113">-Local</span><span class="sxs-lookup"><span data-stu-id="b1da4-113">-Local</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: l

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1da4-114">-Profile</span><span class="sxs-lookup"><span data-stu-id="b1da4-114">-Profile</span></span>
<span data-ttu-id="b1da4-115">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1da4-115">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b1da4-116">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="b1da4-116">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b1da4-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1da4-117">CommonParameters</span></span>
<span data-ttu-id="b1da4-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1da4-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1da4-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1da4-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1da4-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b1da4-120">INPUTS</span></span>

## <span data-ttu-id="b1da4-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b1da4-121">OUTPUTS</span></span>

## <span data-ttu-id="b1da4-122">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b1da4-122">NOTES</span></span>

## <span data-ttu-id="b1da4-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b1da4-123">RELATED LINKS</span></span>

[<span data-ttu-id="b1da4-124">Publikowanie — AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="b1da4-124">Publish-AzureServiceProject</span></span>](./Publish-AzureServiceProject.md)


