---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: BB139312-A536-4B61-A005-6CAF02BE1637
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageFileSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageFileSASToken.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 052eae9a995aafe9d5d966ae5a17aae31a0fc0fc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719547"
---
# <span data-ttu-id="1c423-101">New-AzureStorageFileSASToken</span><span class="sxs-lookup"><span data-stu-id="1c423-101">New-AzureStorageFileSASToken</span></span>

## <span data-ttu-id="1c423-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1c423-102">SYNOPSIS</span></span>
<span data-ttu-id="1c423-103">Generuje token podpisu dostępu współdzielonego dla pliku magazynu.</span><span class="sxs-lookup"><span data-stu-id="1c423-103">Generates a shared access signature token for a Storage file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1c423-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1c423-104">SYNTAX</span></span>

### <span data-ttu-id="1c423-105">NameSasPermission</span><span class="sxs-lookup"><span data-stu-id="1c423-105">NameSasPermission</span></span>
```
New-AzureStorageFileSASToken [-ShareName] <String> [-Path] <String> [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="1c423-106">NameSasPolicy</span><span class="sxs-lookup"><span data-stu-id="1c423-106">NameSasPolicy</span></span>
```
New-AzureStorageFileSASToken [-ShareName] <String> [-Path] <String> -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="1c423-107">FileSasPermission</span><span class="sxs-lookup"><span data-stu-id="1c423-107">FileSasPermission</span></span>
```
New-AzureStorageFileSASToken -File <CloudFile> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri] [<CommonParameters>]
```

### <span data-ttu-id="1c423-108">FileSasPolicy</span><span class="sxs-lookup"><span data-stu-id="1c423-108">FileSasPolicy</span></span>
```
New-AzureStorageFileSASToken -File <CloudFile> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri] [<CommonParameters>]
```

## <span data-ttu-id="1c423-109">Opis</span><span class="sxs-lookup"><span data-stu-id="1c423-109">DESCRIPTION</span></span>
<span data-ttu-id="1c423-110">Polecenie cmdlet **New-AzureStorageFileSASToken** generuje token podpisu dostępu współdzielonego dla pliku magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1c423-110">The **New-AzureStorageFileSASToken** cmdlet generates a shared access signature token for an Azure Storage file.</span></span>

## <span data-ttu-id="1c423-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1c423-111">EXAMPLES</span></span>

### <span data-ttu-id="1c423-112">Przykład 1. Generuj token podpisu dostępu współdzielonego z pełnymi uprawnieniami do plików</span><span class="sxs-lookup"><span data-stu-id="1c423-112">Example 1: Generate a shared access signature token that has full file permissions</span></span>
```
PS C:\> New-AzureStorageFileSASToken -ShareName "ContosoShare" -Path "FilePath" -Permission "rwd"
```

<span data-ttu-id="1c423-113">To polecenie generuje token podpisu dostępu współdzielonego z pełnymi uprawnieniami do pliku o nazwie FilePath.</span><span class="sxs-lookup"><span data-stu-id="1c423-113">This command generates a shared access signature token that has full permissions for the file that is named FilePath.</span></span>

### <span data-ttu-id="1c423-114">Przykład 2: generowanie tokenu podpisu dostępu współdzielonego z limitem czasu</span><span class="sxs-lookup"><span data-stu-id="1c423-114">Example 2: Generate a shared access signature token that has a time limit</span></span>
```
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $StartTime.AddHours(2.0)
PS C:\> New-AzureStorageFileSASToken -ShareName "ContosoShare" -Path "FilePath" -Permission "rwd" -StartTime $StartTime -ExpiryTime $EndTime
```

<span data-ttu-id="1c423-115">Pierwsze polecenie tworzy obiekt **DateTime** przy użyciu Get-Date polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c423-115">The first command creates a **DateTime** object by using the Get-Date cmdlet.</span></span>
<span data-ttu-id="1c423-116">Polecenie zapisuje bieżący czas w zmiennej $StartTime.</span><span class="sxs-lookup"><span data-stu-id="1c423-116">The command stores the current time in the $StartTime variable.</span></span>

<span data-ttu-id="1c423-117">Drugie polecenie dodaje dwie godziny do obiektu w $StartTime, a następnie zapisuje wynik w zmiennej $EndTime.</span><span class="sxs-lookup"><span data-stu-id="1c423-117">The second command adds two hours to the object in $StartTime, and then stores the result in the $EndTime variable.</span></span>
<span data-ttu-id="1c423-118">Ten obiekt jest w przyszłości godziną dwiema godzinami.</span><span class="sxs-lookup"><span data-stu-id="1c423-118">This object is a time two hours in the future.</span></span>

<span data-ttu-id="1c423-119">Trzecie polecenie generuje token podpisu dostępu współdzielonego z określonymi uprawnieniami.</span><span class="sxs-lookup"><span data-stu-id="1c423-119">The third command generates a shared access signature token that has the specified permissions.</span></span>
<span data-ttu-id="1c423-120">Ten token będzie obowiązywał w bieżącym czasie.</span><span class="sxs-lookup"><span data-stu-id="1c423-120">This token becomes valid at the current time.</span></span>
<span data-ttu-id="1c423-121">Token pozostaje ważny do czasu przechowywania w $EndTime.</span><span class="sxs-lookup"><span data-stu-id="1c423-121">The token remains valid until time stored in $EndTime.</span></span>

## <span data-ttu-id="1c423-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1c423-122">PARAMETERS</span></span>

### <span data-ttu-id="1c423-123">-Context</span><span class="sxs-lookup"><span data-stu-id="1c423-123">-Context</span></span>
<span data-ttu-id="1c423-124">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="1c423-124">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="1c423-125">Aby uzyskać kontekst, użyj polecenia cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="1c423-125">To obtain a context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: NameSasPermission, NameSasPolicy
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1c423-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="1c423-126">-ExpiryTime</span></span>
<span data-ttu-id="1c423-127">Określa czas, po upływie którego podpis udostępniony jest nieprawidłowy.</span><span class="sxs-lookup"><span data-stu-id="1c423-127">Specifies the time at which the shared access signature becomes invalid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c423-128">-File (plik)</span><span class="sxs-lookup"><span data-stu-id="1c423-128">-File</span></span>
<span data-ttu-id="1c423-129">Określa obiekt **CloudFile** .</span><span class="sxs-lookup"><span data-stu-id="1c423-129">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="1c423-130">Możesz utworzyć plik w chmurze lub uzyskać go za pomocą polecenia cmdlet Get-AzureStorageFile.</span><span class="sxs-lookup"><span data-stu-id="1c423-130">You can create a cloud file or obtain one by using the Get-AzureStorageFile cmdlet.</span></span>

```yaml
Type: CloudFile
Parameter Sets: FileSasPermission, FileSasPolicy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1c423-131">-FullUri</span><span class="sxs-lookup"><span data-stu-id="1c423-131">-FullUri</span></span>
<span data-ttu-id="1c423-132">Wskazuje, że to polecenie cmdlet zwróci pełny identyfikator URI obiektu BLOB i token podpisu dostępu współdzielonego.</span><span class="sxs-lookup"><span data-stu-id="1c423-132">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="1c423-133">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="1c423-133">-IPAddressOrRange</span></span>
<span data-ttu-id="1c423-134">Określa adres IP lub zakres adresów IP, od których należy akceptować żądania, takie jak 168.1.5.65 lub 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="1c423-134">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="1c423-135">Zakresem jest włącznie.</span><span class="sxs-lookup"><span data-stu-id="1c423-135">The range is inclusive.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c423-136">-Path</span><span class="sxs-lookup"><span data-stu-id="1c423-136">-Path</span></span>
<span data-ttu-id="1c423-137">Określa ścieżkę pliku względem udziału miejsca do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="1c423-137">Specifies the path of the file relative to a Storage share.</span></span>

```yaml
Type: String
Parameter Sets: NameSasPermission, NameSasPolicy
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1c423-138">-Uprawnienie</span><span class="sxs-lookup"><span data-stu-id="1c423-138">-Permission</span></span>
<span data-ttu-id="1c423-139">Określa uprawnienia do pliku magazynu.</span><span class="sxs-lookup"><span data-stu-id="1c423-139">Specifies the permissions for a Storage file.</span></span>

```yaml
Type: String
Parameter Sets: NameSasPermission, FileSasPermission
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c423-140">-Policy</span><span class="sxs-lookup"><span data-stu-id="1c423-140">-Policy</span></span>
<span data-ttu-id="1c423-141">Określa zapisane zasady dostępu do pliku.</span><span class="sxs-lookup"><span data-stu-id="1c423-141">Specifies the stored access policy for a file.</span></span>

```yaml
Type: String
Parameter Sets: NameSasPolicy, FileSasPolicy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c423-142">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="1c423-142">-Protocol</span></span>
<span data-ttu-id="1c423-143">Określa protokół dozwolony dla żądania.</span><span class="sxs-lookup"><span data-stu-id="1c423-143">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="1c423-144">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="1c423-144">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="1c423-145">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="1c423-145">HttpsOnly</span></span>
* <span data-ttu-id="1c423-146">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="1c423-146">HttpsOrHttp</span></span>

<span data-ttu-id="1c423-147">Wartość domyślna to HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="1c423-147">The default value is HttpsOrHttp.</span></span>

```yaml
Type: SharedAccessProtocol
Parameter Sets: (All)
Aliases: 
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c423-148">-Nazwa_udziału</span><span class="sxs-lookup"><span data-stu-id="1c423-148">-ShareName</span></span>
<span data-ttu-id="1c423-149">Określa nazwę udziału magazynu.</span><span class="sxs-lookup"><span data-stu-id="1c423-149">Specifies the name of the Storage share.</span></span>

```yaml
Type: String
Parameter Sets: NameSasPermission, NameSasPolicy
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1c423-150">-StartTime</span><span class="sxs-lookup"><span data-stu-id="1c423-150">-StartTime</span></span>
<span data-ttu-id="1c423-151">Określa czas, po upływie którego podpis udostępniony będzie ważny.</span><span class="sxs-lookup"><span data-stu-id="1c423-151">Specifies the time at which the shared access signature becomes valid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c423-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c423-152">CommonParameters</span></span>
<span data-ttu-id="1c423-153">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c423-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c423-154">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c423-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c423-155">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1c423-155">INPUTS</span></span>

### <span data-ttu-id="1c423-156">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="1c423-156">IStorageContext</span></span>

<span data-ttu-id="1c423-157">Parametr "context" przyjmuje wartość typu "IStorageContext" z potoku</span><span class="sxs-lookup"><span data-stu-id="1c423-157">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="1c423-158">CloudFile</span><span class="sxs-lookup"><span data-stu-id="1c423-158">CloudFile</span></span>

<span data-ttu-id="1c423-159">Parametr "File" przyjmuje wartość typu "CloudFile" z procesu</span><span class="sxs-lookup"><span data-stu-id="1c423-159">Parameter 'File' accepts value of type 'CloudFile' from the pipeline</span></span>

### <span data-ttu-id="1c423-160">Ciąg</span><span class="sxs-lookup"><span data-stu-id="1c423-160">String</span></span>

<span data-ttu-id="1c423-161">Parametr "Path" przyjmuje wartość typu "String" z procesu</span><span class="sxs-lookup"><span data-stu-id="1c423-161">Parameter 'Path' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="1c423-162">Ciąg</span><span class="sxs-lookup"><span data-stu-id="1c423-162">String</span></span>

<span data-ttu-id="1c423-163">Parametr "nazwa_udziału" akceptuje wartość typu "String" z procesu</span><span class="sxs-lookup"><span data-stu-id="1c423-163">Parameter 'ShareName' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="1c423-164">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1c423-164">OUTPUTS</span></span>

### <span data-ttu-id="1c423-165">System. String</span><span class="sxs-lookup"><span data-stu-id="1c423-165">System.String</span></span>

## <span data-ttu-id="1c423-166">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1c423-166">NOTES</span></span>

## <span data-ttu-id="1c423-167">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1c423-167">RELATED LINKS</span></span>

[<span data-ttu-id="1c423-168">Nowe — AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="1c423-168">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="1c423-169">Nowe — AzureStorageShareSASToken</span><span class="sxs-lookup"><span data-stu-id="1c423-169">New-AzureStorageShareSASToken</span></span>](./New-AzureStorageShareSASToken.md)
