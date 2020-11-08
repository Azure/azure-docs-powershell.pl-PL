---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: BBB1A0B7-2F5A-4799-8375-1D775C9D6E2F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 935d9ace51144cdd54cbcf3348ed9fc6b9b4ea02
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054765"
---
# <span data-ttu-id="3a122-101">Set-AzureSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="3a122-101">Set-AzureSchedulerHttpJob</span></span>

## <span data-ttu-id="3a122-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3a122-102">SYNOPSIS</span></span>
<span data-ttu-id="3a122-103">Aktualizuje zadanie harmonogramu z akcją HTTP.</span><span class="sxs-lookup"><span data-stu-id="3a122-103">Updates a scheduler job that has an HTTP action.</span></span>

## <span data-ttu-id="3a122-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3a122-104">SYNTAX</span></span>

### <span data-ttu-id="3a122-105">Wymagane</span><span class="sxs-lookup"><span data-stu-id="3a122-105">Required</span></span>
```
Set-AzureSchedulerHttpJob -Location <String> -JobCollectionName <String> -JobName <String> [-Method <String>]
 [-URI <Uri>] [-RequestBody <String>] [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-ExecutionCount <Int32>] [-EndTime <DateTime>] [-JobState <String>] [-Headers <Hashtable>]
 [-ErrorActionMethod <String>] [-ErrorActionURI <Uri>] [-ErrorActionRequestBody <String>]
 [-ErrorActionHeaders <Hashtable>] [-ErrorActionStorageAccount <String>] [-ErrorActionStorageQueue <String>]
 [-ErrorActionSASToken <String>] [-ErrorActionQueueMessageBody <String>] [-HttpAuthenticationType <String>]
 [-ClientCertificatePfx <Object>] [-ClientCertificatePassword <String>] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="3a122-106">PutPost</span><span class="sxs-lookup"><span data-stu-id="3a122-106">PutPost</span></span>
```
Set-AzureSchedulerHttpJob [-RequestBody <String>] [-JobState <String>] [-Headers <Hashtable>]
 [-ErrorActionHeaders <Hashtable>] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="3a122-107">Cykliczne</span><span class="sxs-lookup"><span data-stu-id="3a122-107">Recurring</span></span>
```
Set-AzureSchedulerHttpJob [-Interval <Int32>] [-Frequency <String>] [-ExecutionCount <Int32>]
 [-EndTime <DateTime>] [-JobState <String>] [-Headers <Hashtable>] [-ErrorActionHeaders <Hashtable>]
 [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="3a122-108">Uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="3a122-108">Authentication</span></span>
```
Set-AzureSchedulerHttpJob [-JobState <String>] [-Headers <Hashtable>] [-ErrorActionHeaders <Hashtable>]
 -HttpAuthenticationType <String> [-ClientCertificatePfx <Object>] [-ClientCertificatePassword <String>]
 [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3a122-109">Opis</span><span class="sxs-lookup"><span data-stu-id="3a122-109">DESCRIPTION</span></span>
<span data-ttu-id="3a122-110">W tym temacie opisano polecenie cmdlet w wersji 0.8.10 modułu PowerShell platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3a122-110">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="3a122-111">Aby uzyskać wersję używanego modułu, należy wpisać w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="3a122-111">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="3a122-112">Polecenie cmdlet **Set-AzureSchedulerHttpJob** aktualizuje zadanie harmonogramu z akcją http.</span><span class="sxs-lookup"><span data-stu-id="3a122-112">The **Set-AzureSchedulerHttpJob** cmdlet updates a scheduler job that has an HTTP action.</span></span>

## <span data-ttu-id="3a122-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3a122-113">EXAMPLES</span></span>

### <span data-ttu-id="3a122-114">Przykład 1. Zmienianie stanu zadania na wyłączone</span><span class="sxs-lookup"><span data-stu-id="3a122-114">Example 1: Change the state of a job to Disabled</span></span>
```
PS C:\> Set-AzureSchedulerHttpJob -Location "North Central US" -JobCollectionName "JobCollection01" -JobName "Job01" -JobState "Disabled"
```

<span data-ttu-id="3a122-115">To polecenie zmienia stan zadania o nazwie Job01 na wyłączone.</span><span class="sxs-lookup"><span data-stu-id="3a122-115">This command changes the state of the job named Job01 to Disabled.</span></span>
<span data-ttu-id="3a122-116">To zadanie jest częścią kolekcji zadań o nazwie JobColleciton01 dla określonej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="3a122-116">That job is part of the job collection named JobColleciton01 for the specified location.</span></span>

### <span data-ttu-id="3a122-117">Przykład 2: aktualizowanie identyfikatora URI zadania</span><span class="sxs-lookup"><span data-stu-id="3a122-117">Example 2: Update the URI of a job</span></span>
```
PS C:\> Set-AzureSchedulerHttpJob -Location "North Central US" -JobCollectionName "JobCollection02" -JobName "Job37" -URI http://www.contoso.com
```

<span data-ttu-id="3a122-118">To polecenie aktualizuje identyfikator URI zadania o nazwie Job01 http://www.contoso.com .</span><span class="sxs-lookup"><span data-stu-id="3a122-118">This command updates the URI of the job named Job01 to be http://www.contoso.com.</span></span>

## <span data-ttu-id="3a122-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3a122-119">PARAMETERS</span></span>

### <span data-ttu-id="3a122-120">-ClientCertificatePassword</span><span class="sxs-lookup"><span data-stu-id="3a122-120">-ClientCertificatePassword</span></span>
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

### <span data-ttu-id="3a122-121">-ClientCertificatePfx</span><span class="sxs-lookup"><span data-stu-id="3a122-121">-ClientCertificatePfx</span></span>
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

### <span data-ttu-id="3a122-122">-EndTime</span><span class="sxs-lookup"><span data-stu-id="3a122-122">-EndTime</span></span>
<span data-ttu-id="3a122-123">Określa czas, jako obiekt **DateTime** , aby harmonogram przestał inicjowanie zadań.</span><span class="sxs-lookup"><span data-stu-id="3a122-123">Specifies a time, as a **DateTime** object, for the scheduler to stop initiating jobs.</span></span>
<span data-ttu-id="3a122-124">Aby uzyskać obiekt **DateTime** , należy użyć polecenia cmdlet **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="3a122-124">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="3a122-125">Aby uzyskać więcej informacji, wpisz tekst `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="3a122-125">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="3a122-126">-ErrorActionHeaders</span><span class="sxs-lookup"><span data-stu-id="3a122-126">-ErrorActionHeaders</span></span>
<span data-ttu-id="3a122-127">Określa nagłówki jako tablicę Hashtable.</span><span class="sxs-lookup"><span data-stu-id="3a122-127">Specifies headers as a hashtable.</span></span>

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

### <span data-ttu-id="3a122-128">-ErrorActionMethod</span><span class="sxs-lookup"><span data-stu-id="3a122-128">-ErrorActionMethod</span></span>
<span data-ttu-id="3a122-129">Określa metodę dla typów akcji HTTP i HTTPS.</span><span class="sxs-lookup"><span data-stu-id="3a122-129">Specifies the method for HTTP and HTTPS action types.</span></span>
<span data-ttu-id="3a122-130">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="3a122-130">Valid values are:</span></span> 

- <span data-ttu-id="3a122-131">Pobierz</span><span class="sxs-lookup"><span data-stu-id="3a122-131">GET</span></span>
- <span data-ttu-id="3a122-132">WPROWADZENIA</span><span class="sxs-lookup"><span data-stu-id="3a122-132">PUT</span></span>
- <span data-ttu-id="3a122-133">WYSYŁK</span><span class="sxs-lookup"><span data-stu-id="3a122-133">POST</span></span>
- <span data-ttu-id="3a122-134">OZNACZENIA</span><span class="sxs-lookup"><span data-stu-id="3a122-134">HEAD</span></span>
- <span data-ttu-id="3a122-135">USUWAĆ</span><span class="sxs-lookup"><span data-stu-id="3a122-135">DELETE</span></span>

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

### <span data-ttu-id="3a122-136">-ErrorActionQueueMessageBody</span><span class="sxs-lookup"><span data-stu-id="3a122-136">-ErrorActionQueueMessageBody</span></span>
<span data-ttu-id="3a122-137">Określa treść akcji zadania magazynu.</span><span class="sxs-lookup"><span data-stu-id="3a122-137">Specifies the body for storage job actions.</span></span>

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

### <span data-ttu-id="3a122-138">-ErrorActionRequestBody</span><span class="sxs-lookup"><span data-stu-id="3a122-138">-ErrorActionRequestBody</span></span>
<span data-ttu-id="3a122-139">Określa treść dla akcji PUT i KSIĘGUJ zadania.</span><span class="sxs-lookup"><span data-stu-id="3a122-139">Specifies the body for PUT and POST job actions.</span></span>

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

### <span data-ttu-id="3a122-140">-ErrorActionSASToken</span><span class="sxs-lookup"><span data-stu-id="3a122-140">-ErrorActionSASToken</span></span>
<span data-ttu-id="3a122-141">Określa token (SAS) (Shared Access Signature) dla kolejki magazynu.</span><span class="sxs-lookup"><span data-stu-id="3a122-141">Specifies the Shared Access Signature (SAS) token for the storage queue.</span></span>

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

### <span data-ttu-id="3a122-142">-ErrorActionStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3a122-142">-ErrorActionStorageAccount</span></span>
<span data-ttu-id="3a122-143">Określa nazwę konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="3a122-143">Specifies the name of the storage account.</span></span>

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

### <span data-ttu-id="3a122-144">-ErrorActionStorageQueue</span><span class="sxs-lookup"><span data-stu-id="3a122-144">-ErrorActionStorageQueue</span></span>
<span data-ttu-id="3a122-145">Określa nazwę kolejki magazynu.</span><span class="sxs-lookup"><span data-stu-id="3a122-145">Specifies the name of the storage queue.</span></span>

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

### <span data-ttu-id="3a122-146">-ErrorActionURI</span><span class="sxs-lookup"><span data-stu-id="3a122-146">-ErrorActionURI</span></span>
<span data-ttu-id="3a122-147">Określa identyfikator URI dla akcji zadania błędu.</span><span class="sxs-lookup"><span data-stu-id="3a122-147">Specifies the URI for the error job action.</span></span>

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

### <span data-ttu-id="3a122-148">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="3a122-148">-ExecutionCount</span></span>
<span data-ttu-id="3a122-149">Określa liczbę wystąpień uruchomionego zadania.</span><span class="sxs-lookup"><span data-stu-id="3a122-149">Specifies the number occurrences of a job that run.</span></span>
<span data-ttu-id="3a122-150">Domyślnie zadanie powtarza się cyklicznie.</span><span class="sxs-lookup"><span data-stu-id="3a122-150">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="3a122-151">-Częstotliwość</span><span class="sxs-lookup"><span data-stu-id="3a122-151">-Frequency</span></span>
<span data-ttu-id="3a122-152">Określa maksymalną częstotliwość dla tego zadania harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="3a122-152">Specifies the maximum frequency for this scheduler job.</span></span>

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

### <span data-ttu-id="3a122-153">-Nagłówki</span><span class="sxs-lookup"><span data-stu-id="3a122-153">-Headers</span></span>
<span data-ttu-id="3a122-154">Określa nagłówki jako tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="3a122-154">Specifies the headers as a hash table.</span></span>

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

### <span data-ttu-id="3a122-155">-HttpAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="3a122-155">-HttpAuthenticationType</span></span>
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

### <span data-ttu-id="3a122-156">-Interval</span><span class="sxs-lookup"><span data-stu-id="3a122-156">-Interval</span></span>
<span data-ttu-id="3a122-157">Określa interwał cyklu z częstotliwością określoną przy użyciu parametru *częstotliwości* .</span><span class="sxs-lookup"><span data-stu-id="3a122-157">Specifies the interval of recurrence at the frequency specified by using the *Frequency* parameter.</span></span>

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

### <span data-ttu-id="3a122-158">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="3a122-158">-JobCollectionName</span></span>
<span data-ttu-id="3a122-159">Określa nazwę kolekcji zawierającej zadanie harmonogramu do zmodyfikowania.</span><span class="sxs-lookup"><span data-stu-id="3a122-159">Specifies the name of the collection that contains the scheduler job to modify.</span></span>

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

### <span data-ttu-id="3a122-160">-JobName</span><span class="sxs-lookup"><span data-stu-id="3a122-160">-JobName</span></span>
<span data-ttu-id="3a122-161">Określa nazwę zadania harmonogramu, które należy zmodyfikować.</span><span class="sxs-lookup"><span data-stu-id="3a122-161">Specifies the name of scheduler job to modify.</span></span>

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

### <span data-ttu-id="3a122-162">-JobState</span><span class="sxs-lookup"><span data-stu-id="3a122-162">-JobState</span></span>
<span data-ttu-id="3a122-163">Określa stan zadania harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="3a122-163">Specifies the state for the scheduler job.</span></span>

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

### <span data-ttu-id="3a122-164">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="3a122-164">-Location</span></span>
<span data-ttu-id="3a122-165">Określa nazwę lokalizacji, w której znajduje się usługa chmury.</span><span class="sxs-lookup"><span data-stu-id="3a122-165">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="3a122-166">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="3a122-166">Valid values are:</span></span> 

- <span data-ttu-id="3a122-167">W dowolnym miejscu w Azji</span><span class="sxs-lookup"><span data-stu-id="3a122-167">Anywhere Asia</span></span>
- <span data-ttu-id="3a122-168">Dowolne miejsce w Europie</span><span class="sxs-lookup"><span data-stu-id="3a122-168">Anywhere Europe</span></span>
- <span data-ttu-id="3a122-169">Dowolne miejsce w USA</span><span class="sxs-lookup"><span data-stu-id="3a122-169">Anywhere US</span></span>
- <span data-ttu-id="3a122-170">Azja Wschodnia</span><span class="sxs-lookup"><span data-stu-id="3a122-170">East Asia</span></span>
- <span data-ttu-id="3a122-171">Wschodnie USA</span><span class="sxs-lookup"><span data-stu-id="3a122-171">East US</span></span>
- <span data-ttu-id="3a122-172">Północno-środkowe USA</span><span class="sxs-lookup"><span data-stu-id="3a122-172">North Central US</span></span>
- <span data-ttu-id="3a122-173">Europa Północna</span><span class="sxs-lookup"><span data-stu-id="3a122-173">North Europe</span></span>
- <span data-ttu-id="3a122-174">Południowa Centrala amerykańska</span><span class="sxs-lookup"><span data-stu-id="3a122-174">South Central US</span></span>
- <span data-ttu-id="3a122-175">Azja Południowo-Wschodnia</span><span class="sxs-lookup"><span data-stu-id="3a122-175">Southeast Asia</span></span>
- <span data-ttu-id="3a122-176">Europa Zachodnia</span><span class="sxs-lookup"><span data-stu-id="3a122-176">West Europe</span></span>
- <span data-ttu-id="3a122-177">Zachodnie USA</span><span class="sxs-lookup"><span data-stu-id="3a122-177">West US</span></span>

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

### <span data-ttu-id="3a122-178">-Method</span><span class="sxs-lookup"><span data-stu-id="3a122-178">-Method</span></span>
<span data-ttu-id="3a122-179">Określa metodę dla typów akcji HTTP i HTTPS.</span><span class="sxs-lookup"><span data-stu-id="3a122-179">Specifies the method for HTTP and HTTPS action types.</span></span>
<span data-ttu-id="3a122-180">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="3a122-180">Valid values are:</span></span> 

- <span data-ttu-id="3a122-181">Pobierz</span><span class="sxs-lookup"><span data-stu-id="3a122-181">GET</span></span>
- <span data-ttu-id="3a122-182">WPROWADZENIA</span><span class="sxs-lookup"><span data-stu-id="3a122-182">PUT</span></span>
- <span data-ttu-id="3a122-183">WYSYŁK</span><span class="sxs-lookup"><span data-stu-id="3a122-183">POST</span></span>
- <span data-ttu-id="3a122-184">OZNACZENIA</span><span class="sxs-lookup"><span data-stu-id="3a122-184">HEAD</span></span>
- <span data-ttu-id="3a122-185">USUWAĆ</span><span class="sxs-lookup"><span data-stu-id="3a122-185">DELETE</span></span>

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

### <span data-ttu-id="3a122-186">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3a122-186">-PassThru</span></span>
<span data-ttu-id="3a122-187">Wskazuje, że to polecenie cmdlet zwraca obiekt reprezentujący element, na którym działa.</span><span class="sxs-lookup"><span data-stu-id="3a122-187">Indicates that this cmdlet returns an object representing the item on which it operates.</span></span>
<span data-ttu-id="3a122-188">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="3a122-188">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3a122-189">-Profile</span><span class="sxs-lookup"><span data-stu-id="3a122-189">-Profile</span></span>
<span data-ttu-id="3a122-190">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a122-190">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3a122-191">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="3a122-191">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3a122-192">-RequestBody</span><span class="sxs-lookup"><span data-stu-id="3a122-192">-RequestBody</span></span>
<span data-ttu-id="3a122-193">Określa treść dla akcji PUT i KSIĘGUJ zadania.</span><span class="sxs-lookup"><span data-stu-id="3a122-193">Specifies the body for PUT and POST job actions.</span></span>

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

### <span data-ttu-id="3a122-194">-StartTime</span><span class="sxs-lookup"><span data-stu-id="3a122-194">-StartTime</span></span>
<span data-ttu-id="3a122-195">Określa godzinę, jako obiekt **DateTime** , w celu rozpoczęcia zadania.</span><span class="sxs-lookup"><span data-stu-id="3a122-195">Specifies a time, as a **DateTime** object, for the job to start.</span></span>

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

### <span data-ttu-id="3a122-196">-URI</span><span class="sxs-lookup"><span data-stu-id="3a122-196">-URI</span></span>
<span data-ttu-id="3a122-197">Określa identyfikator URI dla akcji zadania.</span><span class="sxs-lookup"><span data-stu-id="3a122-197">Specifies a URI for a job action.</span></span>

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

### <span data-ttu-id="3a122-198">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a122-198">CommonParameters</span></span>
<span data-ttu-id="3a122-199">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a122-199">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a122-200">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a122-200">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a122-201">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3a122-201">INPUTS</span></span>

## <span data-ttu-id="3a122-202">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3a122-202">OUTPUTS</span></span>

## <span data-ttu-id="3a122-203">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3a122-203">NOTES</span></span>

## <span data-ttu-id="3a122-204">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3a122-204">RELATED LINKS</span></span>

[<span data-ttu-id="3a122-205">Nowe — AzureSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="3a122-205">New-AzureSchedulerHttpJob</span></span>](./New-AzureSchedulerHttpJob.md)


