---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: BB139312-A536-4B61-A005-6CAF02BE1637
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragefilesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageFileSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageFileSASToken.md
ms.openlocfilehash: fcd58edbb3d6e03becc8e6305f58555fedf36107
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94231630"
---
# <span data-ttu-id="15873-101">New-AzStorageFileSASToken</span><span class="sxs-lookup"><span data-stu-id="15873-101">New-AzStorageFileSASToken</span></span>

## <span data-ttu-id="15873-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="15873-102">SYNOPSIS</span></span>
<span data-ttu-id="15873-103">Generuje token podpisu dostępu współdzielonego dla pliku magazynu.</span><span class="sxs-lookup"><span data-stu-id="15873-103">Generates a shared access signature token for a Storage file.</span></span>

## <span data-ttu-id="15873-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="15873-104">SYNTAX</span></span>

### <span data-ttu-id="15873-105">NameSasPermission</span><span class="sxs-lookup"><span data-stu-id="15873-105">NameSasPermission</span></span>
```
New-AzStorageFileSASToken [-ShareName] <String> [-Path] <String> [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="15873-106">NameSasPolicy</span><span class="sxs-lookup"><span data-stu-id="15873-106">NameSasPolicy</span></span>
```
New-AzStorageFileSASToken [-ShareName] <String> [-Path] <String> -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="15873-107">FileSasPermission</span><span class="sxs-lookup"><span data-stu-id="15873-107">FileSasPermission</span></span>
```
New-AzStorageFileSASToken -File <CloudFile> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="15873-108">FileSasPolicy</span><span class="sxs-lookup"><span data-stu-id="15873-108">FileSasPolicy</span></span>
```
New-AzStorageFileSASToken -File <CloudFile> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="15873-109">Opis</span><span class="sxs-lookup"><span data-stu-id="15873-109">DESCRIPTION</span></span>
<span data-ttu-id="15873-110">Polecenie cmdlet **New-AzStorageFileSASToken** generuje token podpisu dostępu współdzielonego dla pliku magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="15873-110">The **New-AzStorageFileSASToken** cmdlet generates a shared access signature token for an Azure Storage file.</span></span>

## <span data-ttu-id="15873-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="15873-111">EXAMPLES</span></span>

### <span data-ttu-id="15873-112">Przykład 1. Generuj token podpisu dostępu współdzielonego z pełnymi uprawnieniami do plików</span><span class="sxs-lookup"><span data-stu-id="15873-112">Example 1: Generate a shared access signature token that has full file permissions</span></span>
```
PS C:\> New-AzStorageFileSASToken -ShareName "ContosoShare" -Path "FilePath" -Permission "rwd"
```

<span data-ttu-id="15873-113">To polecenie generuje token podpisu dostępu współdzielonego z pełnymi uprawnieniami do pliku o nazwie FilePath.</span><span class="sxs-lookup"><span data-stu-id="15873-113">This command generates a shared access signature token that has full permissions for the file that is named FilePath.</span></span>

### <span data-ttu-id="15873-114">Przykład 2: generowanie tokenu podpisu dostępu współdzielonego z limitem czasu</span><span class="sxs-lookup"><span data-stu-id="15873-114">Example 2: Generate a shared access signature token that has a time limit</span></span>
```
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $StartTime.AddHours(2.0)
PS C:\> New-AzStorageFileSASToken -ShareName "ContosoShare" -Path "FilePath" -Permission "rwd" -StartTime $StartTime -ExpiryTime $EndTime
```

<span data-ttu-id="15873-115">Pierwsze polecenie tworzy obiekt **DateTime** przy użyciu Get-Date polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="15873-115">The first command creates a **DateTime** object by using the Get-Date cmdlet.</span></span>
<span data-ttu-id="15873-116">Polecenie zapisuje bieżący czas w zmiennej $StartTime.</span><span class="sxs-lookup"><span data-stu-id="15873-116">The command stores the current time in the $StartTime variable.</span></span>
<span data-ttu-id="15873-117">Drugie polecenie dodaje dwie godziny do obiektu w $StartTime, a następnie zapisuje wynik w zmiennej $EndTime.</span><span class="sxs-lookup"><span data-stu-id="15873-117">The second command adds two hours to the object in $StartTime, and then stores the result in the $EndTime variable.</span></span>
<span data-ttu-id="15873-118">Ten obiekt jest w przyszłości godziną dwiema godzinami.</span><span class="sxs-lookup"><span data-stu-id="15873-118">This object is a time two hours in the future.</span></span>
<span data-ttu-id="15873-119">Trzecie polecenie generuje token podpisu dostępu współdzielonego z określonymi uprawnieniami.</span><span class="sxs-lookup"><span data-stu-id="15873-119">The third command generates a shared access signature token that has the specified permissions.</span></span>
<span data-ttu-id="15873-120">Ten token będzie obowiązywał w bieżącym czasie.</span><span class="sxs-lookup"><span data-stu-id="15873-120">This token becomes valid at the current time.</span></span>
<span data-ttu-id="15873-121">Token pozostaje ważny do czasu przechowywania w $EndTime.</span><span class="sxs-lookup"><span data-stu-id="15873-121">The token remains valid until time stored in $EndTime.</span></span>

## <span data-ttu-id="15873-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="15873-122">PARAMETERS</span></span>

### <span data-ttu-id="15873-123">-Context</span><span class="sxs-lookup"><span data-stu-id="15873-123">-Context</span></span>
<span data-ttu-id="15873-124">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="15873-124">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="15873-125">Aby uzyskać kontekst, użyj polecenia cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="15873-125">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: NameSasPermission, NameSasPolicy
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="15873-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15873-126">-DefaultProfile</span></span>
<span data-ttu-id="15873-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="15873-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15873-128">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="15873-128">-ExpiryTime</span></span>
<span data-ttu-id="15873-129">Określa czas, po upływie którego podpis udostępniony jest nieprawidłowy.</span><span class="sxs-lookup"><span data-stu-id="15873-129">Specifies the time at which the shared access signature becomes invalid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15873-130">-File (plik)</span><span class="sxs-lookup"><span data-stu-id="15873-130">-File</span></span>
<span data-ttu-id="15873-131">Określa obiekt **CloudFile** .</span><span class="sxs-lookup"><span data-stu-id="15873-131">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="15873-132">Możesz utworzyć plik w chmurze lub uzyskać go za pomocą polecenia cmdlet Get-AzStorageFile.</span><span class="sxs-lookup"><span data-stu-id="15873-132">You can create a cloud file or obtain one by using the Get-AzStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: FileSasPermission, FileSasPolicy
Aliases: CloudFile

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="15873-133">-FullUri</span><span class="sxs-lookup"><span data-stu-id="15873-133">-FullUri</span></span>
<span data-ttu-id="15873-134">Wskazuje, że to polecenie cmdlet zwróci pełny identyfikator URI obiektu BLOB i token podpisu dostępu współdzielonego.</span><span class="sxs-lookup"><span data-stu-id="15873-134">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15873-135">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="15873-135">-IPAddressOrRange</span></span>
<span data-ttu-id="15873-136">Określa adres IP lub zakres adresów IP, od których należy akceptować żądania, takie jak 168.1.5.65 lub 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="15873-136">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="15873-137">Zakresem jest włącznie.</span><span class="sxs-lookup"><span data-stu-id="15873-137">The range is inclusive.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15873-138">-Path</span><span class="sxs-lookup"><span data-stu-id="15873-138">-Path</span></span>
<span data-ttu-id="15873-139">Określa ścieżkę pliku względem udziału miejsca do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="15873-139">Specifies the path of the file relative to a Storage share.</span></span>

```yaml
Type: System.String
Parameter Sets: NameSasPermission, NameSasPolicy
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="15873-140">-Uprawnienie</span><span class="sxs-lookup"><span data-stu-id="15873-140">-Permission</span></span>
<span data-ttu-id="15873-141">Określa uprawnienia do pliku magazynu.</span><span class="sxs-lookup"><span data-stu-id="15873-141">Specifies the permissions for a Storage file.</span></span>
<span data-ttu-id="15873-142">Ważne jest, aby zwrócić uwagę, że jest to ciąg, taki jak `rwd` (na przykład odczyt, zapis i usuwanie).</span><span class="sxs-lookup"><span data-stu-id="15873-142">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

```yaml
Type: System.String
Parameter Sets: NameSasPermission, FileSasPermission
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15873-143">-Policy</span><span class="sxs-lookup"><span data-stu-id="15873-143">-Policy</span></span>
<span data-ttu-id="15873-144">Określa zapisane zasady dostępu do pliku.</span><span class="sxs-lookup"><span data-stu-id="15873-144">Specifies the stored access policy for a file.</span></span>

```yaml
Type: System.String
Parameter Sets: NameSasPolicy, FileSasPolicy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15873-145">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="15873-145">-Protocol</span></span>
<span data-ttu-id="15873-146">Określa protokół dozwolony dla żądania.</span><span class="sxs-lookup"><span data-stu-id="15873-146">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="15873-147">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="15873-147">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="15873-148">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="15873-148">HttpsOnly</span></span>
* <span data-ttu-id="15873-149">HttpsOrHttp wartość domyślna to HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="15873-149">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Storage.SharedAccessProtocol]
Parameter Sets: (All)
Aliases:
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15873-150">-Nazwa_udziału</span><span class="sxs-lookup"><span data-stu-id="15873-150">-ShareName</span></span>
<span data-ttu-id="15873-151">Określa nazwę udziału magazynu.</span><span class="sxs-lookup"><span data-stu-id="15873-151">Specifies the name of the Storage share.</span></span>

```yaml
Type: System.String
Parameter Sets: NameSasPermission, NameSasPolicy
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="15873-152">-StartTime</span><span class="sxs-lookup"><span data-stu-id="15873-152">-StartTime</span></span>
<span data-ttu-id="15873-153">Określa czas, po upływie którego podpis udostępniony będzie ważny.</span><span class="sxs-lookup"><span data-stu-id="15873-153">Specifies the time at which the shared access signature becomes valid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15873-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15873-154">CommonParameters</span></span>
<span data-ttu-id="15873-155">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15873-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15873-156">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15873-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15873-157">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="15873-157">INPUTS</span></span>

### <span data-ttu-id="15873-158">System. String</span><span class="sxs-lookup"><span data-stu-id="15873-158">System.String</span></span>

### <span data-ttu-id="15873-159">Microsoft. Azure. Storage. File. CloudFile</span><span class="sxs-lookup"><span data-stu-id="15873-159">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="15873-160">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="15873-160">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="15873-161">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="15873-161">OUTPUTS</span></span>

### <span data-ttu-id="15873-162">System. String</span><span class="sxs-lookup"><span data-stu-id="15873-162">System.String</span></span>

## <span data-ttu-id="15873-163">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="15873-163">NOTES</span></span>

## <span data-ttu-id="15873-164">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="15873-164">RELATED LINKS</span></span>

[<span data-ttu-id="15873-165">Nowe — AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="15873-165">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="15873-166">Nowe — AzStorageShareSASToken</span><span class="sxs-lookup"><span data-stu-id="15873-166">New-AzStorageShareSASToken</span></span>](./New-AzStorageShareSASToken.md)
