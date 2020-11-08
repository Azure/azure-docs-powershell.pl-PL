---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: A2CBF963-1FAE-41B0-964E-EFF52076AB32
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2c4bb84111b8ec22b1b529622e61ca476cf6081b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055473"
---
# <span data-ttu-id="84353-101">Get-AzureWebsiteJobHistory</span><span class="sxs-lookup"><span data-stu-id="84353-101">Get-AzureWebsiteJobHistory</span></span>

## <span data-ttu-id="84353-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="84353-102">SYNOPSIS</span></span>
<span data-ttu-id="84353-103">Pobiera historię zadań sieci Web.</span><span class="sxs-lookup"><span data-stu-id="84353-103">Gets a web job history.</span></span>

## <span data-ttu-id="84353-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="84353-104">SYNTAX</span></span>

### <span data-ttu-id="84353-105">HistoryParameterSetName</span><span class="sxs-lookup"><span data-stu-id="84353-105">HistoryParameterSetName</span></span>
```
Get-AzureWebsiteJobHistory -JobName <String> [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="84353-106">RunIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="84353-106">RunIdParameterSetName</span></span>
```
Get-AzureWebsiteJobHistory -JobName <String> -RunId <String> [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="84353-107">LatestParameterSetName</span><span class="sxs-lookup"><span data-stu-id="84353-107">LatestParameterSetName</span></span>
```
Get-AzureWebsiteJobHistory -JobName <String> [-Latest] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="84353-108">Opis</span><span class="sxs-lookup"><span data-stu-id="84353-108">DESCRIPTION</span></span>
<span data-ttu-id="84353-109">Pobiera historię zadań sieci Web.</span><span class="sxs-lookup"><span data-stu-id="84353-109">Gets a web job history.</span></span>

## <span data-ttu-id="84353-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="84353-110">EXAMPLES</span></span>

### <span data-ttu-id="84353-111">Przykład 1: uzyskiwanie pełnej historii zadania sieci Web</span><span class="sxs-lookup"><span data-stu-id="84353-111">Example 1: Get complete history for a web job</span></span>
```
PS C:\> Get-AzureWebsiteJobHistory -Name MyWebsite -JobName MyWebJob
```

<span data-ttu-id="84353-112">Pobiera kompletną historię dla MyWebJob.</span><span class="sxs-lookup"><span data-stu-id="84353-112">Gets complete history for MyWebJob.</span></span>

### <span data-ttu-id="84353-113">Przykład 2: uzyskiwanie najnowszego uruchomienia zadania sieci Web</span><span class="sxs-lookup"><span data-stu-id="84353-113">Example 2: Get latest run for a web job</span></span>
```
PS C:\> Get-AzureWebsiteJobHistory -Name MyWebsite -JobName MyWebJob -Latest
```

<span data-ttu-id="84353-114">Pobiera najnowsze informacje o uruchomieniu MyWebJob.</span><span class="sxs-lookup"><span data-stu-id="84353-114">Gets latest run info for MyWebJob.</span></span>

### <span data-ttu-id="84353-115">Przykład 3: uzyskiwanie określonego uruchomienia zadania sieci Web</span><span class="sxs-lookup"><span data-stu-id="84353-115">Example 3: Get specific run for a web job</span></span>
```
PS C:\> Get-AzureWebsiteJobHistory -Name MyWebsite -JobName MyWebJob -RunId 10
```

<span data-ttu-id="84353-116">Pobiera wszystkie informacje o uruchomieniu z identyfikatorem 10 dla MyWebJob.</span><span class="sxs-lookup"><span data-stu-id="84353-116">Gets all info about run with id 10 for MyWebJob.</span></span>

## <span data-ttu-id="84353-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="84353-117">PARAMETERS</span></span>

### <span data-ttu-id="84353-118">-JobName</span><span class="sxs-lookup"><span data-stu-id="84353-118">-JobName</span></span>
<span data-ttu-id="84353-119">Nazwa zadania w sieci Web.</span><span class="sxs-lookup"><span data-stu-id="84353-119">The web job name.</span></span>

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

### <span data-ttu-id="84353-120">-Najnowsze</span><span class="sxs-lookup"><span data-stu-id="84353-120">-Latest</span></span>
<span data-ttu-id="84353-121">Jeśli ta pole jest określona, zwróć najnowszą historię przebiegu.</span><span class="sxs-lookup"><span data-stu-id="84353-121">If specified, return the latest run history.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: LatestParameterSetName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84353-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="84353-122">-Name</span></span>
<span data-ttu-id="84353-123">Nazwa witryny sieci Web usługi Azure.</span><span class="sxs-lookup"><span data-stu-id="84353-123">The name of the Azure website.</span></span>

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

### <span data-ttu-id="84353-124">-Profile</span><span class="sxs-lookup"><span data-stu-id="84353-124">-Profile</span></span>
<span data-ttu-id="84353-125">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="84353-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="84353-126">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="84353-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="84353-127">-RunId</span><span class="sxs-lookup"><span data-stu-id="84353-127">-RunId</span></span>
<span data-ttu-id="84353-128">Określa identyfikator historii uruchamiania, który ma być wyświetlany.</span><span class="sxs-lookup"><span data-stu-id="84353-128">Specifies the ID of the run history you want to see.</span></span>

```yaml
Type: String
Parameter Sets: RunIdParameterSetName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84353-129">-Slot</span><span class="sxs-lookup"><span data-stu-id="84353-129">-Slot</span></span>
<span data-ttu-id="84353-130">Nazwa gniazda witryny sieci Web usługi Azure.</span><span class="sxs-lookup"><span data-stu-id="84353-130">The slot name of the Azure website.</span></span>

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

### <span data-ttu-id="84353-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84353-131">CommonParameters</span></span>
<span data-ttu-id="84353-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84353-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84353-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84353-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84353-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="84353-134">INPUTS</span></span>

## <span data-ttu-id="84353-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="84353-135">OUTPUTS</span></span>

## <span data-ttu-id="84353-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="84353-136">NOTES</span></span>

## <span data-ttu-id="84353-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="84353-137">RELATED LINKS</span></span>

[<span data-ttu-id="84353-138">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="84353-138">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="84353-139">Nowe — AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="84353-139">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="84353-140">Get-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="84353-140">Get-AzureWebsiteJob</span></span>](./Get-AzureWebsiteJob.md)

[<span data-ttu-id="84353-141">Nowe — AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="84353-141">New-AzureWebsiteJob</span></span>](./New-AzureWebsiteJob.md)

[<span data-ttu-id="84353-142">Remove-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="84353-142">Remove-AzureWebsiteJob</span></span>](./Remove-AzureWebsiteJob.md)


