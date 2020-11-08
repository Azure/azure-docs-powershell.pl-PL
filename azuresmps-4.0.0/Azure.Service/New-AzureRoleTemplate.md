---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: E499868E-A745-4CA4-A717-C33C3B94A2C8
online version: ''
schema: 2.0.0
ms.openlocfilehash: b80071bb82ebbb960be5b5b4fcc854dc47c9ed9d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054958"
---
# <span data-ttu-id="90493-101">New-AzureRoleTemplate</span><span class="sxs-lookup"><span data-stu-id="90493-101">New-AzureRoleTemplate</span></span>

## <span data-ttu-id="90493-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="90493-102">SYNOPSIS</span></span>
<span data-ttu-id="90493-103">Tworzy szablony ról witryny sieci Web i procesu roboczego.</span><span class="sxs-lookup"><span data-stu-id="90493-103">Creates web and worker role templates.</span></span>

## <span data-ttu-id="90493-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="90493-104">SYNTAX</span></span>

### <span data-ttu-id="90493-105">Rola</span><span class="sxs-lookup"><span data-stu-id="90493-105">WebRole</span></span>
```
New-AzureRoleTemplate [-Web] [-Output <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="90493-106">WorkerRole</span><span class="sxs-lookup"><span data-stu-id="90493-106">WorkerRole</span></span>
```
New-AzureRoleTemplate [-Worker] [-Output <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="90493-107">Opis</span><span class="sxs-lookup"><span data-stu-id="90493-107">DESCRIPTION</span></span>
<span data-ttu-id="90493-108">W tym temacie opisano polecenie cmdlet w wersji 0.8.10 modułu PowerShell platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="90493-108">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="90493-109">Aby uzyskać wersję używanego modułu, należy wpisać w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="90493-109">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="90493-110">Polecenie cmdlet **New-AzureRoleTemplate** tworzy szablony ról sieci Web i procesu roboczego.</span><span class="sxs-lookup"><span data-stu-id="90493-110">The **New-AzureRoleTemplate** cmdlet creates web and worker role templates.</span></span>

## <span data-ttu-id="90493-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="90493-111">EXAMPLES</span></span>

### <span data-ttu-id="90493-112">Przykład 1. Tworzenie szablonu roli sieci Web</span><span class="sxs-lookup"><span data-stu-id="90493-112">Example 1: Create a web role template</span></span>
```
PS C:\> New-AzureRoleTemplate -Web
```

<span data-ttu-id="90493-113">W tym przykładzie jest tworzony nowy szablon roli sieci Web w folderze o nazwie WebRoleTemplate w bieżącym katalogu.</span><span class="sxs-lookup"><span data-stu-id="90493-113">This example creates a new web role template in a folder named WebRoleTemplate in the current directory.</span></span>

### <span data-ttu-id="90493-114">Przykład 2: Tworzenie szablonu roli pracownika</span><span class="sxs-lookup"><span data-stu-id="90493-114">Example 2: Create a worker role template</span></span>
```
PS C:\> New-AzureRoleTemplate -Worker
```

<span data-ttu-id="90493-115">W tym przykładzie jest tworzony nowy szablon roli procesu roboczego w folderze o nazwie WebRoleTemplate w bieżącym katalogu.</span><span class="sxs-lookup"><span data-stu-id="90493-115">This example creates a new worker role template in a folder named WebRoleTemplate in the current directory.</span></span>

### <span data-ttu-id="90493-116">Przykład 3: Tworzenie szablonu roli w katalogu niestandardowym</span><span class="sxs-lookup"><span data-stu-id="90493-116">Example 3: Create a role template in a custom directory</span></span>
```
PS C:\> New-AzureRoleTemplate -Web -Output C:\MyWebRoleTemplate
```

<span data-ttu-id="90493-117">W tym przykładzie jest tworzony nowy szablon roli sieci Web w katalogu o nazwie MyWebRoleTemplate, a nie w bieżącym katalogu.</span><span class="sxs-lookup"><span data-stu-id="90493-117">This example creates a new web role template in directory named MyWebRoleTemplate, instead of in the current directory.</span></span>

## <span data-ttu-id="90493-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="90493-118">PARAMETERS</span></span>

### <span data-ttu-id="90493-119">— Dane wyjściowe</span><span class="sxs-lookup"><span data-stu-id="90493-119">-Output</span></span>
<span data-ttu-id="90493-120">Określa ścieżkę wyjściową utworzonego szablonu.</span><span class="sxs-lookup"><span data-stu-id="90493-120">Specifies the output path of generated template.</span></span>

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

### <span data-ttu-id="90493-121">-Profile</span><span class="sxs-lookup"><span data-stu-id="90493-121">-Profile</span></span>
<span data-ttu-id="90493-122">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="90493-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="90493-123">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="90493-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="90493-124">-Web</span><span class="sxs-lookup"><span data-stu-id="90493-124">-Web</span></span>
<span data-ttu-id="90493-125">Określa, że chcesz utworzyć szablon roli sieci Web.</span><span class="sxs-lookup"><span data-stu-id="90493-125">Specifies that you want to create a web role template.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WebRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90493-126">-Pracownik</span><span class="sxs-lookup"><span data-stu-id="90493-126">-Worker</span></span>
<span data-ttu-id="90493-127">Określa, że chcesz utworzyć szablon roli pracownika.</span><span class="sxs-lookup"><span data-stu-id="90493-127">Specifies that you want to create a worker role template.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WorkerRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90493-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90493-128">CommonParameters</span></span>
<span data-ttu-id="90493-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90493-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90493-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90493-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90493-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="90493-131">INPUTS</span></span>

## <span data-ttu-id="90493-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="90493-132">OUTPUTS</span></span>

## <span data-ttu-id="90493-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="90493-133">NOTES</span></span>

## <span data-ttu-id="90493-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="90493-134">RELATED LINKS</span></span>

[<span data-ttu-id="90493-135">Dodaj-AzureWebRole</span><span class="sxs-lookup"><span data-stu-id="90493-135">Add-AzureWebRole</span></span>](./Add-AzureWebRole.md)

[<span data-ttu-id="90493-136">Dodaj-AzureWorkerRole</span><span class="sxs-lookup"><span data-stu-id="90493-136">Add-AzureWorkerRole</span></span>](./Add-AzureWorkerRole.md)


