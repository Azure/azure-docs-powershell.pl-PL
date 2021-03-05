---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: BB139312-A536-4B61-A005-6CAF02BE1637
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstoragefilesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageFileSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageFileSASToken.md
ms.openlocfilehash: ec5f290a6c45725dfed369058d5e00bbee016f9e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002449"
---
# <span data-ttu-id="fedd0-101">New-AzStorageFileSASToken</span><span class="sxs-lookup"><span data-stu-id="fedd0-101">New-AzStorageFileSASToken</span></span>

## <span data-ttu-id="fedd0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fedd0-102">SYNOPSIS</span></span>
<span data-ttu-id="fedd0-103">Generuje token podpisu dostępu udostępnionego dla pliku magazynu.</span><span class="sxs-lookup"><span data-stu-id="fedd0-103">Generates a shared access signature token for a Storage file.</span></span>

## <span data-ttu-id="fedd0-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="fedd0-104">SYNTAX</span></span>

### <span data-ttu-id="fedd0-105">NameSasPermission</span><span class="sxs-lookup"><span data-stu-id="fedd0-105">NameSasPermission</span></span>
```
New-AzStorageFileSASToken [-ShareName] <String> [-Path] <String> [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fedd0-106">NameSasPolicy</span><span class="sxs-lookup"><span data-stu-id="fedd0-106">NameSasPolicy</span></span>
```
New-AzStorageFileSASToken [-ShareName] <String> [-Path] <String> -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fedd0-107">FileSasPermission</span><span class="sxs-lookup"><span data-stu-id="fedd0-107">FileSasPermission</span></span>
```
New-AzStorageFileSASToken -File <CloudFile> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fedd0-108">FileSasPolicy</span><span class="sxs-lookup"><span data-stu-id="fedd0-108">FileSasPolicy</span></span>
```
New-AzStorageFileSASToken -File <CloudFile> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fedd0-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="fedd0-109">DESCRIPTION</span></span>
<span data-ttu-id="fedd0-110">Polecenie **cmdlet New-AzStorageFileSASToken** generuje token podpisu dostępu udostępnionego dla pliku magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="fedd0-110">The **New-AzStorageFileSASToken** cmdlet generates a shared access signature token for an Azure Storage file.</span></span>

## <span data-ttu-id="fedd0-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="fedd0-111">EXAMPLES</span></span>

### <span data-ttu-id="fedd0-112">Przykład 1. Generowanie tokenu podpisu dostępu udostępnionego z pełnymi uprawnieniami do pliku</span><span class="sxs-lookup"><span data-stu-id="fedd0-112">Example 1: Generate a shared access signature token that has full file permissions</span></span>
```
PS C:\> New-AzStorageFileSASToken -ShareName "ContosoShare" -Path "FilePath" -Permission "rwd"
```

<span data-ttu-id="fedd0-113">To polecenie generuje token podpisu dostępu udostępnionego, który ma pełne uprawnienia do pliku o nazwie FilePath.</span><span class="sxs-lookup"><span data-stu-id="fedd0-113">This command generates a shared access signature token that has full permissions for the file that is named FilePath.</span></span>

### <span data-ttu-id="fedd0-114">Przykład 2. Generowanie tokenu podpisu dostępu udostępnionego z limitem czasu</span><span class="sxs-lookup"><span data-stu-id="fedd0-114">Example 2: Generate a shared access signature token that has a time limit</span></span>
```
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $StartTime.AddHours(2.0)
PS C:\> New-AzStorageFileSASToken -ShareName "ContosoShare" -Path "FilePath" -Permission "rwd" -StartTime $StartTime -ExpiryTime $EndTime
```

<span data-ttu-id="fedd0-115">Pierwsze polecenie tworzy obiekt **DateTime** przy użyciu Get-Date cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fedd0-115">The first command creates a **DateTime** object by using the Get-Date cmdlet.</span></span>
<span data-ttu-id="fedd0-116">Polecenie przechowuje bieżącą wartość czasu w $StartTime zmienną.</span><span class="sxs-lookup"><span data-stu-id="fedd0-116">The command stores the current time in the $StartTime variable.</span></span>
<span data-ttu-id="fedd0-117">Drugie polecenie dodaje dwie godziny do obiektu w $StartTime, a następnie zapisuje wynik w $EndTime zmienną.</span><span class="sxs-lookup"><span data-stu-id="fedd0-117">The second command adds two hours to the object in $StartTime, and then stores the result in the $EndTime variable.</span></span>
<span data-ttu-id="fedd0-118">Ten obiekt będzie o dwie godziny późniejszą godziną.</span><span class="sxs-lookup"><span data-stu-id="fedd0-118">This object is a time two hours in the future.</span></span>
<span data-ttu-id="fedd0-119">Trzecie polecenie generuje token podpisu dostępu udostępnionego, który ma określone uprawnienia.</span><span class="sxs-lookup"><span data-stu-id="fedd0-119">The third command generates a shared access signature token that has the specified permissions.</span></span>
<span data-ttu-id="fedd0-120">Ten token stanie się prawidłowy w bieżącej chwili.</span><span class="sxs-lookup"><span data-stu-id="fedd0-120">This token becomes valid at the current time.</span></span>
<span data-ttu-id="fedd0-121">Token jest ważny do momentu przechowywania go w $EndTime.</span><span class="sxs-lookup"><span data-stu-id="fedd0-121">The token remains valid until time stored in $EndTime.</span></span>

## <span data-ttu-id="fedd0-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fedd0-122">PARAMETERS</span></span>

### <span data-ttu-id="fedd0-123">— kontekst</span><span class="sxs-lookup"><span data-stu-id="fedd0-123">-Context</span></span>
<span data-ttu-id="fedd0-124">Określa kontekst magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="fedd0-124">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="fedd0-125">Aby uzyskać kontekst, użyj polecenia cmdlet New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fedd0-125">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="fedd0-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fedd0-126">-DefaultProfile</span></span>
<span data-ttu-id="fedd0-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="fedd0-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fedd0-128">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="fedd0-128">-ExpiryTime</span></span>
<span data-ttu-id="fedd0-129">Określa czas, w którym podpis dostępu udostępnionego staje się nieprawidłowy.</span><span class="sxs-lookup"><span data-stu-id="fedd0-129">Specifies the time at which the shared access signature becomes invalid.</span></span>

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

### <span data-ttu-id="fedd0-130">— Plik</span><span class="sxs-lookup"><span data-stu-id="fedd0-130">-File</span></span>
<span data-ttu-id="fedd0-131">Określa obiekt **CloudFile.**</span><span class="sxs-lookup"><span data-stu-id="fedd0-131">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="fedd0-132">Możesz utworzyć plik w chmurze lub uzyskać go za pomocą Get-AzStorageFile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fedd0-132">You can create a cloud file or obtain one by using the Get-AzStorageFile cmdlet.</span></span>

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

### <span data-ttu-id="fedd0-133">-FullUri</span><span class="sxs-lookup"><span data-stu-id="fedd0-133">-FullUri</span></span>
<span data-ttu-id="fedd0-134">Wskazuje, że to polecenie cmdlet zwraca pełny adres URI obiektu blob i token podpisu dostępu udostępnionego.</span><span class="sxs-lookup"><span data-stu-id="fedd0-134">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="fedd0-135">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="fedd0-135">-IPAddressOrRange</span></span>
<span data-ttu-id="fedd0-136">Określa adres IP lub zakres adresów IP, z których mają być akceptowane żądania, na przykład 168.1.5.65 lub 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="fedd0-136">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="fedd0-137">Zakres jest włącznie.</span><span class="sxs-lookup"><span data-stu-id="fedd0-137">The range is inclusive.</span></span>

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

### <span data-ttu-id="fedd0-138">— Ścieżka</span><span class="sxs-lookup"><span data-stu-id="fedd0-138">-Path</span></span>
<span data-ttu-id="fedd0-139">Określa ścieżkę pliku względem udziału magazynu.</span><span class="sxs-lookup"><span data-stu-id="fedd0-139">Specifies the path of the file relative to a Storage share.</span></span>

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

### <span data-ttu-id="fedd0-140">— Uprawnienie</span><span class="sxs-lookup"><span data-stu-id="fedd0-140">-Permission</span></span>
<span data-ttu-id="fedd0-141">Określa uprawnienia do pliku magazynu.</span><span class="sxs-lookup"><span data-stu-id="fedd0-141">Specifies the permissions for a Storage file.</span></span>
<span data-ttu-id="fedd0-142">Należy pamiętać, że jest to ciąg, taki jak `rwd` (w przypadku odczytu, zapisu i usunięcia).</span><span class="sxs-lookup"><span data-stu-id="fedd0-142">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="fedd0-143">— Zasady</span><span class="sxs-lookup"><span data-stu-id="fedd0-143">-Policy</span></span>
<span data-ttu-id="fedd0-144">Określa zasady przechowywanego dostępu dla pliku.</span><span class="sxs-lookup"><span data-stu-id="fedd0-144">Specifies the stored access policy for a file.</span></span>

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

### <span data-ttu-id="fedd0-145">— Protokół</span><span class="sxs-lookup"><span data-stu-id="fedd0-145">-Protocol</span></span>
<span data-ttu-id="fedd0-146">Określa protokół dozwolony dla żądania.</span><span class="sxs-lookup"><span data-stu-id="fedd0-146">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="fedd0-147">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="fedd0-147">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="fedd0-148">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="fedd0-148">HttpsOnly</span></span>
* <span data-ttu-id="fedd0-149">HttpsOrHttp Wartość domyślna to httpsorhttp.</span><span class="sxs-lookup"><span data-stu-id="fedd0-149">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="fedd0-150">-ShareName</span><span class="sxs-lookup"><span data-stu-id="fedd0-150">-ShareName</span></span>
<span data-ttu-id="fedd0-151">Określa nazwę udziału magazynu.</span><span class="sxs-lookup"><span data-stu-id="fedd0-151">Specifies the name of the Storage share.</span></span>

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

### <span data-ttu-id="fedd0-152">— StartTime</span><span class="sxs-lookup"><span data-stu-id="fedd0-152">-StartTime</span></span>
<span data-ttu-id="fedd0-153">Określa czas, w którym podpis dostępu udostępnionego stanie się prawidłowy.</span><span class="sxs-lookup"><span data-stu-id="fedd0-153">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="fedd0-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fedd0-154">CommonParameters</span></span>
<span data-ttu-id="fedd0-155">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fedd0-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fedd0-156">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fedd0-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fedd0-157">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fedd0-157">INPUTS</span></span>

### <span data-ttu-id="fedd0-158">System.String</span><span class="sxs-lookup"><span data-stu-id="fedd0-158">System.String</span></span>

### <span data-ttu-id="fedd0-159">Microsoft.Azure.Storage.File.CloudFile</span><span class="sxs-lookup"><span data-stu-id="fedd0-159">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="fedd0-160">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="fedd0-160">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="fedd0-161">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fedd0-161">OUTPUTS</span></span>

### <span data-ttu-id="fedd0-162">System.String</span><span class="sxs-lookup"><span data-stu-id="fedd0-162">System.String</span></span>

## <span data-ttu-id="fedd0-163">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="fedd0-163">NOTES</span></span>

## <span data-ttu-id="fedd0-164">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fedd0-164">RELATED LINKS</span></span>

[<span data-ttu-id="fedd0-165">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="fedd0-165">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="fedd0-166">New-AzstorageSharesasToken</span><span class="sxs-lookup"><span data-stu-id="fedd0-166">New-AzStorageShareSASToken</span></span>](./New-AzStorageShareSASToken.md)
