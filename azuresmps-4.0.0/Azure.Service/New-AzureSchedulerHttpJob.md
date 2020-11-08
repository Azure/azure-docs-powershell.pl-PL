---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: C608BBDD-DC2B-4BEF-812D-0BAE94FB4395
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0f5332c18d2d47096f246485ac0d811548f70aa9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054870"
---
# <span data-ttu-id="e0ede-101">New-AzureSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="e0ede-101">New-AzureSchedulerHttpJob</span></span>

## <span data-ttu-id="e0ede-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e0ede-102">SYNOPSIS</span></span>
<span data-ttu-id="e0ede-103">Tworzy zadanie harmonogramu z akcją HTTP.</span><span class="sxs-lookup"><span data-stu-id="e0ede-103">Creates a scheduler job that has an HTTP action.</span></span>

## <span data-ttu-id="e0ede-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e0ede-104">SYNTAX</span></span>

### <span data-ttu-id="e0ede-105">Wymagane</span><span class="sxs-lookup"><span data-stu-id="e0ede-105">Required</span></span>
```
New-AzureSchedulerHttpJob -Location <String> -JobCollectionName <String> -JobName <String> -Method <String>
 -URI <Uri> [-RequestBody <String>] [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-ExecutionCount <Int32>] [-EndTime <DateTime>] [-JobState <String>] [-Headers <Hashtable>]
 [-ErrorActionMethod <String>] [-ErrorActionURI <Uri>] [-ErrorActionRequestBody <String>]
 [-ErrorActionHeaders <Hashtable>] [-ErrorActionStorageAccount <String>] [-ErrorActionStorageQueue <String>]
 [-ErrorActionSASToken <String>] [-ErrorActionQueueMessageBody <String>] [-HttpAuthenticationType <String>]
 [-ClientCertificatePfx <Object>] [-ClientCertificatePassword <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="e0ede-106">PutPost</span><span class="sxs-lookup"><span data-stu-id="e0ede-106">PutPost</span></span>
```
New-AzureSchedulerHttpJob [-RequestBody <String>] [-JobState <String>] [-Headers <Hashtable>]
 [-ErrorActionHeaders <Hashtable>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="e0ede-107">Cykliczne</span><span class="sxs-lookup"><span data-stu-id="e0ede-107">Recurring</span></span>
```
New-AzureSchedulerHttpJob [-Interval <Int32>] [-Frequency <String>] [-ExecutionCount <Int32>]
 [-EndTime <DateTime>] [-JobState <String>] [-Headers <Hashtable>] [-ErrorActionHeaders <Hashtable>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="e0ede-108">Uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="e0ede-108">Authentication</span></span>
```
New-AzureSchedulerHttpJob [-JobState <String>] [-Headers <Hashtable>] [-ErrorActionHeaders <Hashtable>]
 -HttpAuthenticationType <String> [-ClientCertificatePfx <Object>] [-ClientCertificatePassword <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e0ede-109">Opis</span><span class="sxs-lookup"><span data-stu-id="e0ede-109">DESCRIPTION</span></span>
<span data-ttu-id="e0ede-110">W tym temacie opisano polecenie cmdlet w wersji 0.8.10 modułu PowerShell platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="e0ede-110">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="e0ede-111">Aby uzyskać wersję używanego modułu, należy wpisać w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="e0ede-111">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="e0ede-112">Polecenie cmdlet **New-AzureSchedulerHttpJob** tworzy zadanie harmonogramu z akcją http.</span><span class="sxs-lookup"><span data-stu-id="e0ede-112">The **New-AzureSchedulerHttpJob** cmdlet creates a scheduler job that has an HTTP action.</span></span>

## <span data-ttu-id="e0ede-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e0ede-113">EXAMPLES</span></span>

### <span data-ttu-id="e0ede-114">Przykład 1. Tworzenie zadania HTTP</span><span class="sxs-lookup"><span data-stu-id="e0ede-114">Example 1: Create an HTTP job</span></span>
```
PS C:\> New-AzureSchedulerHttpJob -JobCollectionName "JobCollection01" -JobName "Job01" -Location "North Central US" -Method "GET" -URI http://www.contoso.com
```

<span data-ttu-id="e0ede-115">To polecenie tworzy zadanie HTTP harmonogramu w kolekcji zadań o nazwie JobCollection01.</span><span class="sxs-lookup"><span data-stu-id="e0ede-115">This command creates a scheduler HTTP job in the job collection named JobCollection01.</span></span>
<span data-ttu-id="e0ede-116">Polecenie określa identyfikator URI i określa metodę GET AS.</span><span class="sxs-lookup"><span data-stu-id="e0ede-116">The command specifies a URI and specifies GET as the method.</span></span>

### <span data-ttu-id="e0ede-117">Przykład 2: Tworzenie zadania HTTP dla określonej liczby uruchomień</span><span class="sxs-lookup"><span data-stu-id="e0ede-117">Example 2: Create an HTTP job for a specific run count</span></span>
```
PS C:\> New-AzureSchedulerHttpJob -JobCollectionName "JobCollection01 -JobName "Job23" -Location "North Central US" -Method "GET" -URI http://www.contoso.com -ExecutionCount 20
```

<span data-ttu-id="e0ede-118">To polecenie tworzy zadanie http harmonogramu w kolekcji zadań o nazwie JobCollection01.</span><span class="sxs-lookup"><span data-stu-id="e0ede-118">This command creates scheduler http job in the job collection named JobCollection01.</span></span>
<span data-ttu-id="e0ede-119">Polecenie określa identyfikator URI i określa metodę GET AS.</span><span class="sxs-lookup"><span data-stu-id="e0ede-119">The command specifies a URI and specifies GET as the method.</span></span>
<span data-ttu-id="e0ede-120">To polecenie powoduje, że zadanie jest uruchamiane 20 razy.</span><span class="sxs-lookup"><span data-stu-id="e0ede-120">This command causes the job to run 20 times.</span></span>

## <span data-ttu-id="e0ede-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e0ede-121">PARAMETERS</span></span>

### <span data-ttu-id="e0ede-122">-ClientCertificatePassword</span><span class="sxs-lookup"><span data-stu-id="e0ede-122">-ClientCertificatePassword</span></span>
```yaml
Type: String
Parameter Sets: Required, Authentication
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0ede-123">-ClientCertificatePfx</span><span class="sxs-lookup"><span data-stu-id="e0ede-123">-ClientCertificatePfx</span></span>
```yaml
Type: Object
Parameter Sets: Required, Authentication
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0ede-124">-EndTime</span><span class="sxs-lookup"><span data-stu-id="e0ede-124">-EndTime</span></span>
<span data-ttu-id="e0ede-125">Określa czas, jako obiekt **DateTime** , aby harmonogram przestał inicjowanie zadań.</span><span class="sxs-lookup"><span data-stu-id="e0ede-125">Specifies a time, as a **DateTime** object, for the scheduler to stop initiating jobs.</span></span>
<span data-ttu-id="e0ede-126">Aby uzyskać obiekt **DateTime** , należy użyć polecenia cmdlet **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="e0ede-126">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="e0ede-127">Aby uzyskać więcej informacji, wpisz tekst `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="e0ede-127">For more information, type `Get-Help Get-Date`.</span></span>

```yaml
Type: DateTime
Parameter Sets: Required, Recurring
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0ede-128">-ErrorActionHeaders</span><span class="sxs-lookup"><span data-stu-id="e0ede-128">-ErrorActionHeaders</span></span>
<span data-ttu-id="e0ede-129">Określa nagłówki jako tablicę Hashtable.</span><span class="sxs-lookup"><span data-stu-id="e0ede-129">Specifies headers as a hashtable.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0ede-130">-ErrorActionMethod</span><span class="sxs-lookup"><span data-stu-id="e0ede-130">-ErrorActionMethod</span></span>
<span data-ttu-id="e0ede-131">Określa metodę dla typów akcji HTTP i HTTPS.</span><span class="sxs-lookup"><span data-stu-id="e0ede-131">Specifies the method for HTTP and HTTPS action types.</span></span>
<span data-ttu-id="e0ede-132">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="e0ede-132">Valid values are:</span></span> 

- <span data-ttu-id="e0ede-133">Pobierz</span><span class="sxs-lookup"><span data-stu-id="e0ede-133">GET</span></span>
- <span data-ttu-id="e0ede-134">WPROWADZENIA</span><span class="sxs-lookup"><span data-stu-id="e0ede-134">PUT</span></span>
- <span data-ttu-id="e0ede-135">WYSYŁK</span><span class="sxs-lookup"><span data-stu-id="e0ede-135">POST</span></span>
- <span data-ttu-id="e0ede-136">OZNACZENIA</span><span class="sxs-lookup"><span data-stu-id="e0ede-136">HEAD</span></span>
- <span data-ttu-id="e0ede-137">USUWAĆ</span><span class="sxs-lookup"><span data-stu-id="e0ede-137">DELETE</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0ede-138">-ErrorActionQueueMessageBody</span><span class="sxs-lookup"><span data-stu-id="e0ede-138">-ErrorActionQueueMessageBody</span></span>
<span data-ttu-id="e0ede-139">Określa treść akcji zadania magazynu.</span><span class="sxs-lookup"><span data-stu-id="e0ede-139">Specifies the body for storage job actions.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0ede-140">-ErrorActionRequestBody</span><span class="sxs-lookup"><span data-stu-id="e0ede-140">-ErrorActionRequestBody</span></span>
<span data-ttu-id="e0ede-141">Określa treść dla akcji PUT i KSIĘGUJ zadania.</span><span class="sxs-lookup"><span data-stu-id="e0ede-141">Specifies the body for PUT and POST job actions.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0ede-142">-ErrorActionSASToken</span><span class="sxs-lookup"><span data-stu-id="e0ede-142">-ErrorActionSASToken</span></span>
<span data-ttu-id="e0ede-143">Określa token (SAS) (Shared Access Signature) dla kolejki magazynu.</span><span class="sxs-lookup"><span data-stu-id="e0ede-143">Specifies the Shared Access Signature (SAS) token for the storage queue.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0ede-144">-ErrorActionStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e0ede-144">-ErrorActionStorageAccount</span></span>
<span data-ttu-id="e0ede-145">Określa nazwę konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="e0ede-145">Specifies the name of the storage account.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0ede-146">-ErrorActionStorageQueue</span><span class="sxs-lookup"><span data-stu-id="e0ede-146">-ErrorActionStorageQueue</span></span>
<span data-ttu-id="e0ede-147">Określa nazwę kolejki magazynu.</span><span class="sxs-lookup"><span data-stu-id="e0ede-147">Specifies the name of the storage queue.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0ede-148">-ErrorActionURI</span><span class="sxs-lookup"><span data-stu-id="e0ede-148">-ErrorActionURI</span></span>
<span data-ttu-id="e0ede-149">Określa identyfikator URI dla akcji zadania błędu.</span><span class="sxs-lookup"><span data-stu-id="e0ede-149">Specifies the URI for the error job action.</span></span>

```yaml
Type: Uri
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0ede-150">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="e0ede-150">-ExecutionCount</span></span>
<span data-ttu-id="e0ede-151">Określa liczbę wystąpień uruchomionego zadania.</span><span class="sxs-lookup"><span data-stu-id="e0ede-151">Specifies the number occurrences of a job that run.</span></span>
<span data-ttu-id="e0ede-152">Domyślnie zadanie powtarza się cyklicznie.</span><span class="sxs-lookup"><span data-stu-id="e0ede-152">By default, a job recurs indefinitely.</span></span>

```yaml
Type: Int32
Parameter Sets: Required, Recurring
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0ede-153">-Częstotliwość</span><span class="sxs-lookup"><span data-stu-id="e0ede-153">-Frequency</span></span>
<span data-ttu-id="e0ede-154">Określa maksymalną częstotliwość dla tego zadania harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="e0ede-154">Specifies the maximum frequency for this scheduler job.</span></span>

```yaml
Type: String
Parameter Sets: Required, Recurring
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0ede-155">-Nagłówki</span><span class="sxs-lookup"><span data-stu-id="e0ede-155">-Headers</span></span>
<span data-ttu-id="e0ede-156">Określa nagłówki jako tablicę Hashtable.</span><span class="sxs-lookup"><span data-stu-id="e0ede-156">Specifies the headers as a hashtable.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0ede-157">-HttpAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="e0ede-157">-HttpAuthenticationType</span></span>
```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Authentication
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0ede-158">-Interval</span><span class="sxs-lookup"><span data-stu-id="e0ede-158">-Interval</span></span>
<span data-ttu-id="e0ede-159">Określa interwał cyklu z częstotliwością określoną przy użyciu parametru *częstotliwości* .</span><span class="sxs-lookup"><span data-stu-id="e0ede-159">Specifies the interval of recurrence at the frequency specified by using the *Frequency* parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: Required, Recurring
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0ede-160">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="e0ede-160">-JobCollectionName</span></span>
<span data-ttu-id="e0ede-161">Określa nazwę kolekcji, która ma zawierać zadanie harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="e0ede-161">Specifies the name of the collection to contain the scheduler job.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0ede-162">-JobName</span><span class="sxs-lookup"><span data-stu-id="e0ede-162">-JobName</span></span>
<span data-ttu-id="e0ede-163">Określa nazwę zadania harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="e0ede-163">Specifies the name for the scheduler job.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0ede-164">-JobState</span><span class="sxs-lookup"><span data-stu-id="e0ede-164">-JobState</span></span>
<span data-ttu-id="e0ede-165">Określa stan zadania harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="e0ede-165">Specifies the state for the scheduler job.</span></span>

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

### <span data-ttu-id="e0ede-166">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="e0ede-166">-Location</span></span>
<span data-ttu-id="e0ede-167">Określa nazwę lokalizacji, w której znajduje się usługa chmury.</span><span class="sxs-lookup"><span data-stu-id="e0ede-167">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="e0ede-168">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="e0ede-168">Valid values are:</span></span> 

- <span data-ttu-id="e0ede-169">W dowolnym miejscu w Azji</span><span class="sxs-lookup"><span data-stu-id="e0ede-169">Anywhere Asia</span></span>
- <span data-ttu-id="e0ede-170">Dowolne miejsce w Europie</span><span class="sxs-lookup"><span data-stu-id="e0ede-170">Anywhere Europe</span></span>
- <span data-ttu-id="e0ede-171">Dowolne miejsce w USA</span><span class="sxs-lookup"><span data-stu-id="e0ede-171">Anywhere US</span></span>
- <span data-ttu-id="e0ede-172">Azja Wschodnia</span><span class="sxs-lookup"><span data-stu-id="e0ede-172">East Asia</span></span>
- <span data-ttu-id="e0ede-173">Wschodnie USA</span><span class="sxs-lookup"><span data-stu-id="e0ede-173">East US</span></span>
- <span data-ttu-id="e0ede-174">Północno-środkowe USA</span><span class="sxs-lookup"><span data-stu-id="e0ede-174">North Central US</span></span>
- <span data-ttu-id="e0ede-175">Europa Północna</span><span class="sxs-lookup"><span data-stu-id="e0ede-175">North Europe</span></span>
- <span data-ttu-id="e0ede-176">Południowa Centrala amerykańska</span><span class="sxs-lookup"><span data-stu-id="e0ede-176">South Central US</span></span>
- <span data-ttu-id="e0ede-177">Azja Południowo-Wschodnia</span><span class="sxs-lookup"><span data-stu-id="e0ede-177">Southeast Asia</span></span>
- <span data-ttu-id="e0ede-178">Europa Zachodnia</span><span class="sxs-lookup"><span data-stu-id="e0ede-178">West Europe</span></span>
- <span data-ttu-id="e0ede-179">Zachodnie USA</span><span class="sxs-lookup"><span data-stu-id="e0ede-179">West US</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0ede-180">-Method</span><span class="sxs-lookup"><span data-stu-id="e0ede-180">-Method</span></span>
<span data-ttu-id="e0ede-181">Określa metodę dla typów akcji HTTP i HTTPS.</span><span class="sxs-lookup"><span data-stu-id="e0ede-181">Specifies the method for HTTP and HTTPS action types.</span></span>
<span data-ttu-id="e0ede-182">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="e0ede-182">Valid values are:</span></span> 

- <span data-ttu-id="e0ede-183">Pobierz</span><span class="sxs-lookup"><span data-stu-id="e0ede-183">GET</span></span>
- <span data-ttu-id="e0ede-184">WPROWADZENIA</span><span class="sxs-lookup"><span data-stu-id="e0ede-184">PUT</span></span>
- <span data-ttu-id="e0ede-185">WYSYŁK</span><span class="sxs-lookup"><span data-stu-id="e0ede-185">POST</span></span>
- <span data-ttu-id="e0ede-186">OZNACZENIA</span><span class="sxs-lookup"><span data-stu-id="e0ede-186">HEAD</span></span>
- <span data-ttu-id="e0ede-187">USUWAĆ</span><span class="sxs-lookup"><span data-stu-id="e0ede-187">DELETE</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0ede-188">-Profile</span><span class="sxs-lookup"><span data-stu-id="e0ede-188">-Profile</span></span>
<span data-ttu-id="e0ede-189">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0ede-189">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e0ede-190">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="e0ede-190">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e0ede-191">-RequestBody</span><span class="sxs-lookup"><span data-stu-id="e0ede-191">-RequestBody</span></span>
<span data-ttu-id="e0ede-192">Określa treść dla akcji PUT i KSIĘGUJ zadania.</span><span class="sxs-lookup"><span data-stu-id="e0ede-192">Specifies the body for PUT and POST job actions.</span></span>

```yaml
Type: String
Parameter Sets: Required, PutPost
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0ede-193">-StartTime</span><span class="sxs-lookup"><span data-stu-id="e0ede-193">-StartTime</span></span>
<span data-ttu-id="e0ede-194">Określa godzinę, jako obiekt **DateTime** , w celu rozpoczęcia zadania.</span><span class="sxs-lookup"><span data-stu-id="e0ede-194">Specifies a time, as a **DateTime** object, for the job to start.</span></span>

```yaml
Type: DateTime
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0ede-195">-URI</span><span class="sxs-lookup"><span data-stu-id="e0ede-195">-URI</span></span>
<span data-ttu-id="e0ede-196">Określa identyfikator URI dla akcji zadania.</span><span class="sxs-lookup"><span data-stu-id="e0ede-196">Specifies a URI for a job action.</span></span>

```yaml
Type: Uri
Parameter Sets: Required
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0ede-197">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0ede-197">CommonParameters</span></span>
<span data-ttu-id="e0ede-198">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0ede-198">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0ede-199">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0ede-199">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0ede-200">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e0ede-200">INPUTS</span></span>

## <span data-ttu-id="e0ede-201">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e0ede-201">OUTPUTS</span></span>

## <span data-ttu-id="e0ede-202">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e0ede-202">NOTES</span></span>

## <span data-ttu-id="e0ede-203">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e0ede-203">RELATED LINKS</span></span>

[<span data-ttu-id="e0ede-204">Set-AzureSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="e0ede-204">Set-AzureSchedulerHttpJob</span></span>](./Set-AzureSchedulerHttpJob.md)


