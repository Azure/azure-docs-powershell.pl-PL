---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 2261AD64-196A-402E-9703-EFB3A6D75FA7
online version: ''
schema: 2.0.0
ms.openlocfilehash: d83ed3e336ca72e38fc16c27ec696eea0f84f746
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055184"
---
# <span data-ttu-id="b318f-101">New-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="b318f-101">New-AzureServiceProject</span></span>

## <span data-ttu-id="b318f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b318f-102">SYNOPSIS</span></span>
<span data-ttu-id="b318f-103">Tworzy wymagane pliki i konfigurację dla nowej usługi.</span><span class="sxs-lookup"><span data-stu-id="b318f-103">Creates the required files and configuration for a new service.</span></span>

## <span data-ttu-id="b318f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b318f-104">SYNTAX</span></span>

```
New-AzureServiceProject -ServiceName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b318f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b318f-105">DESCRIPTION</span></span>
<span data-ttu-id="b318f-106">W tym temacie opisano polecenie cmdlet w wersji 0.8.10 modułu PowerShell platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b318f-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="b318f-107">Aby uzyskać wersję używanego modułu, należy wpisać w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="b318f-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="b318f-108">Polecenie cmdlet **New-AzureServiceProject** tworzy wymagane pliki i konfigurację dla nowej usługi Azure w bieżącym katalogu.</span><span class="sxs-lookup"><span data-stu-id="b318f-108">The **New-AzureServiceProject** cmdlet creates the required files and configuration for a new Azure service in the current directory.</span></span>

## <span data-ttu-id="b318f-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b318f-109">EXAMPLES</span></span>

### <span data-ttu-id="b318f-110">Przykład 1. Tworzenie szkieletów dla usługi</span><span class="sxs-lookup"><span data-stu-id="b318f-110">Example 1: Create scaffolding for a service</span></span>
```
PS C:\> New-AzureServiceProject MyService1
```

<span data-ttu-id="b318f-111">W tym przykładzie przedstawiono tworzenie szkieletów dla nowej usługi platformy Azure o nazwie MyService1 w bieżącym katalogu.</span><span class="sxs-lookup"><span data-stu-id="b318f-111">This example creates scaffolding for a new Azure service named MyService1 in the current directory.</span></span>

## <span data-ttu-id="b318f-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b318f-112">PARAMETERS</span></span>

### <span data-ttu-id="b318f-113">-Profile</span><span class="sxs-lookup"><span data-stu-id="b318f-113">-Profile</span></span>
<span data-ttu-id="b318f-114">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b318f-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b318f-115">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="b318f-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b318f-116">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="b318f-116">-ServiceName</span></span>
<span data-ttu-id="b318f-117">Określa nazwę usługi.</span><span class="sxs-lookup"><span data-stu-id="b318f-117">Specifies the name of the service.</span></span>
<span data-ttu-id="b318f-118">Określa pierwszą sekcję nazwy hosta w usłudze (na przykład name.cloudapp.net) oraz katalog, który będzie zawierać usługę.</span><span class="sxs-lookup"><span data-stu-id="b318f-118">It determines the first section of the hostname for your service (for example, name.cloudapp.net), and the directory that will contain your service.</span></span>
<span data-ttu-id="b318f-119">Nazwa może zawierać tylko litery, cyfry i znaki kreski (-).</span><span class="sxs-lookup"><span data-stu-id="b318f-119">The name can contain only letters, digits, and the dash character (-).</span></span>

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

### <span data-ttu-id="b318f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b318f-120">CommonParameters</span></span>
<span data-ttu-id="b318f-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b318f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b318f-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b318f-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b318f-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b318f-123">INPUTS</span></span>

## <span data-ttu-id="b318f-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b318f-124">OUTPUTS</span></span>

## <span data-ttu-id="b318f-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b318f-125">NOTES</span></span>

## <span data-ttu-id="b318f-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b318f-126">RELATED LINKS</span></span>

[<span data-ttu-id="b318f-127">Dodaj-AzureNodeWebRole</span><span class="sxs-lookup"><span data-stu-id="b318f-127">Add-AzureNodeWebRole</span></span>](./Add-AzureNodeWebRole.md)

[<span data-ttu-id="b318f-128">Dodaj-AzureNodeWorkerRole</span><span class="sxs-lookup"><span data-stu-id="b318f-128">Add-AzureNodeWorkerRole</span></span>](./Add-AzureNodeWorkerRole.md)

[<span data-ttu-id="b318f-129">Publikowanie — AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="b318f-129">Publish-AzureServiceProject</span></span>](./Publish-AzureServiceProject.md)

[<span data-ttu-id="b318f-130">Set-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="b318f-130">Set-AzureServiceProject</span></span>](./Set-AzureServiceProject.md)

[<span data-ttu-id="b318f-131">Set-AzureServiceProjectRole</span><span class="sxs-lookup"><span data-stu-id="b318f-131">Set-AzureServiceProjectRole</span></span>](./Set-AzureServiceProjectRole.md)


