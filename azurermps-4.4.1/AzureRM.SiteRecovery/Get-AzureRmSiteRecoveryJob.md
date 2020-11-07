---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: B5CA6FD9-49EE-4115-8477-551CE5D8E6CE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryJob.md
ms.openlocfilehash: 2365b806bd274bb9cc18f84c83a29423408780d2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716871"
---
# <span data-ttu-id="4f709-101">Get-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="4f709-101">Get-AzureRmSiteRecoveryJob</span></span>

## <span data-ttu-id="4f709-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4f709-102">SYNOPSIS</span></span>
<span data-ttu-id="4f709-103">Pobiera informacje o operacjach dotyczących bieżącego magazynu odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="4f709-103">Gets the operation information for the current Site Recovery vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4f709-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4f709-104">SYNTAX</span></span>

### <span data-ttu-id="4f709-105">ByParam (domyślny)</span><span class="sxs-lookup"><span data-stu-id="4f709-105">ByParam (Default)</span></span>
```
Get-AzureRmSiteRecoveryJob [-StartTime <DateTime>] [-EndTime <DateTime>] [-TargetObjectId <String>]
 [-State <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4f709-106">ByName</span><span class="sxs-lookup"><span data-stu-id="4f709-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4f709-107">ByObject</span><span class="sxs-lookup"><span data-stu-id="4f709-107">ByObject</span></span>
```
Get-AzureRmSiteRecoveryJob -Job <ASRJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4f709-108">Opis</span><span class="sxs-lookup"><span data-stu-id="4f709-108">DESCRIPTION</span></span>
<span data-ttu-id="4f709-109">Polecenie cmdlet **Get-AzureRmSiteRecoveryJob** pobiera zadania odzyskiwania witryny Azure.</span><span class="sxs-lookup"><span data-stu-id="4f709-109">The **Get-AzureRmSiteRecoveryJob** cmdlet gets Azure Site Recovery jobs.</span></span>
<span data-ttu-id="4f709-110">Za pomocą tego polecenia cmdlet można wyświetlać informacje o operacjach dotyczących bieżącego magazynu odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="4f709-110">You can use this cmdlet to view the operation information for the current Site Recovery vault.</span></span>

## <span data-ttu-id="4f709-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4f709-111">EXAMPLES</span></span>

## <span data-ttu-id="4f709-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4f709-112">PARAMETERS</span></span>

### <span data-ttu-id="4f709-113">-EndTime</span><span class="sxs-lookup"><span data-stu-id="4f709-113">-EndTime</span></span>
<span data-ttu-id="4f709-114">Określa czas zakończenia zadań.</span><span class="sxs-lookup"><span data-stu-id="4f709-114">Specifies the end time for the jobs.</span></span>
<span data-ttu-id="4f709-115">To polecenie cmdlet umożliwia pobieranie wszystkich zadań rozpoczętych przed określonym terminem.</span><span class="sxs-lookup"><span data-stu-id="4f709-115">This cmdlet gets all jobs that started before the specified time.</span></span>
<span data-ttu-id="4f709-116">Aby uzyskać obiekt **DateTime** dla tego parametru, użyj polecenia cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="4f709-116">To obtain a **DateTime** object for this parameter, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="4f709-117">Aby uzyskać więcej informacji, wpisz tekst `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="4f709-117">For more information, type `Get-Help Get-Date`.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f709-118">— Zadanie</span><span class="sxs-lookup"><span data-stu-id="4f709-118">-Job</span></span>
<span data-ttu-id="4f709-119">Określa zadanie odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="4f709-119">Specifies the Site Recovery job.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRJob
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4f709-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4f709-120">-Name</span></span>
<span data-ttu-id="4f709-121">Określa unikatową nazwę identyfikującą zadanie.</span><span class="sxs-lookup"><span data-stu-id="4f709-121">Specifies a unique name that identifies the job.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f709-122">-StartTime</span><span class="sxs-lookup"><span data-stu-id="4f709-122">-StartTime</span></span>
<span data-ttu-id="4f709-123">Określa czas rozpoczęcia zadań.</span><span class="sxs-lookup"><span data-stu-id="4f709-123">Specifies the start time for the jobs.</span></span>
<span data-ttu-id="4f709-124">To polecenie cmdlet umożliwia pobieranie wszystkich zadań uruchomionych po określonym czasie.</span><span class="sxs-lookup"><span data-stu-id="4f709-124">This cmdlet gets all jobs that started after the specified time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f709-125">-State</span><span class="sxs-lookup"><span data-stu-id="4f709-125">-State</span></span>
<span data-ttu-id="4f709-126">Określa stan wejścia zadania odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="4f709-126">Specifies the input state for a Site Recovery job.</span></span>
<span data-ttu-id="4f709-127">To polecenie cmdlet umożliwia pobieranie wszystkich zadań zgodnych z określonym stanem.</span><span class="sxs-lookup"><span data-stu-id="4f709-127">This cmdlet gets all jobs that match the specified state.</span></span>
<span data-ttu-id="4f709-128">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="4f709-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4f709-129">NotStarted</span><span class="sxs-lookup"><span data-stu-id="4f709-129">NotStarted</span></span>
- <span data-ttu-id="4f709-130">W trakcie</span><span class="sxs-lookup"><span data-stu-id="4f709-130">InProgress</span></span>
- <span data-ttu-id="4f709-131">Doszło</span><span class="sxs-lookup"><span data-stu-id="4f709-131">Succeeded</span></span>
- <span data-ttu-id="4f709-132">Pozostałe</span><span class="sxs-lookup"><span data-stu-id="4f709-132">Other</span></span>
- <span data-ttu-id="4f709-133">Nie powiodło się</span><span class="sxs-lookup"><span data-stu-id="4f709-133">Failed</span></span>
- <span data-ttu-id="4f709-134">Anulowania</span><span class="sxs-lookup"><span data-stu-id="4f709-134">Cancelled</span></span>
- <span data-ttu-id="4f709-135">Zawiesin</span><span class="sxs-lookup"><span data-stu-id="4f709-135">Suspended</span></span>

```yaml
Type: System.String
Parameter Sets: ByParam
Aliases: 
Accepted values: NotStarted, InProgress, Succeeded, Other, Failed, Cancelled, Suspended

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f709-136">-TargetObjectId</span><span class="sxs-lookup"><span data-stu-id="4f709-136">-TargetObjectId</span></span>
<span data-ttu-id="4f709-137">Określa identyfikator obiektu wskazywanego przez zadanie.</span><span class="sxs-lookup"><span data-stu-id="4f709-137">Specifies the ID of the object targeted by the job.</span></span>

```yaml
Type: System.String
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f709-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f709-138">-DefaultProfile</span></span>
<span data-ttu-id="4f709-139">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4f709-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f709-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f709-140">CommonParameters</span></span>
<span data-ttu-id="4f709-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f709-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f709-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f709-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f709-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4f709-143">INPUTS</span></span>

### <span data-ttu-id="4f709-144">ASRJob</span><span class="sxs-lookup"><span data-stu-id="4f709-144">ASRJob</span></span>
<span data-ttu-id="4f709-145">Parametr "zadanie" akceptuje wartość typu "ASRJob" z potoku.</span><span class="sxs-lookup"><span data-stu-id="4f709-145">Parameter 'Job' accepts value of type 'ASRJob' from the pipeline</span></span>

## <span data-ttu-id="4f709-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4f709-146">OUTPUTS</span></span>

### <span data-ttu-id="4f709-147">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. SiteRecovery. ASRJob]</span><span class="sxs-lookup"><span data-stu-id="4f709-147">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRJob]</span></span>

## <span data-ttu-id="4f709-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4f709-148">NOTES</span></span>

## <span data-ttu-id="4f709-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4f709-149">RELATED LINKS</span></span>

[<span data-ttu-id="4f709-150">Restart-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="4f709-150">Restart-AzureRmSiteRecoveryJob</span></span>](./Restart-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="4f709-151">Życiorys — AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="4f709-151">Resume-AzureRmSiteRecoveryJob</span></span>](./Resume-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="4f709-152">Zatrzymaj — AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="4f709-152">Stop-AzureRmSiteRecoveryJob</span></span>](./Stop-AzureRmSiteRecoveryJob.md)