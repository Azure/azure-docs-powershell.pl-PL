---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: BDF42420-3616-4A64-9562-1A896F828728
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragesharesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageShareSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageShareSASToken.md
ms.openlocfilehash: 8dbb6f79a61d388aec033030de471092fa16ba77
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100241843"
---
# <span data-ttu-id="4bb8b-101">New-AzStorageShareSASToken</span><span class="sxs-lookup"><span data-stu-id="4bb8b-101">New-AzStorageShareSASToken</span></span>

## <span data-ttu-id="4bb8b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4bb8b-102">SYNOPSIS</span></span>
<span data-ttu-id="4bb8b-103">Wygeneruj token podpisu dostępu udostępnionego dla udziału magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="4bb8b-103">Generate Shared Access Signature token for Azure Storage share.</span></span>

## <span data-ttu-id="4bb8b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4bb8b-104">SYNTAX</span></span>

### <span data-ttu-id="4bb8b-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="4bb8b-105">SasPolicy</span></span>
```
New-AzStorageShareSASToken [-ShareName] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4bb8b-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="4bb8b-106">SasPermission</span></span>
```
New-AzStorageShareSASToken [-ShareName] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4bb8b-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="4bb8b-107">DESCRIPTION</span></span>
<span data-ttu-id="4bb8b-108">Polecenie **cmdlet New-AzStorageShareSASToken** generuje token podpisu dostępu udostępnionego dla udziału magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="4bb8b-108">The **New-AzStorageShareSASToken** cmdlet generates a shared access signature token for an Azure Storage share.</span></span>

## <span data-ttu-id="4bb8b-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4bb8b-109">EXAMPLES</span></span>

### <span data-ttu-id="4bb8b-110">Przykład 1. Generowanie tokenu podpisu dostępu udostępnionego dla udziału</span><span class="sxs-lookup"><span data-stu-id="4bb8b-110">Example 1: Generate a shared access signature token for a share</span></span>
```
PS C:\>New-AzStorageShareSASToken -ShareName "ContosoShare" -Permission "rwdl"
```

<span data-ttu-id="4bb8b-111">To polecenie tworzy token podpisu dostępu udostępnionego dla udziału o nazwie ContosoShare.</span><span class="sxs-lookup"><span data-stu-id="4bb8b-111">This command creates a shared access signature token for the share named ContosoShare.</span></span>

### <span data-ttu-id="4bb8b-112">Przykład 2. Generowanie wielu tokenów podpisu dostępu udostępnionego przy użyciu potoku</span><span class="sxs-lookup"><span data-stu-id="4bb8b-112">Example 2: Generate multiple shared access signature token by using the pipeline</span></span>
```
PS C:\>Get-AzStorageShare -Prefix "test" | New-AzStorageShareSASToken -Permission "rwdl"
```

<span data-ttu-id="4bb8b-113">To polecenie pobiera wszystkie udziały magazynu zgodne z testem prefiksu.</span><span class="sxs-lookup"><span data-stu-id="4bb8b-113">This command gets all the Storage shares that match the prefix test.</span></span>
<span data-ttu-id="4bb8b-114">Polecenie przekazuje je do bieżącego polecenia cmdlet przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="4bb8b-114">The command passes them to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="4bb8b-115">Bieżące polecenie cmdlet tworzy token dostępu udostępnionego dla każdego udziału magazynu, który ma określone uprawnienia.</span><span class="sxs-lookup"><span data-stu-id="4bb8b-115">The current cmdlet creates a shared access token for each Storage share that has the specified permissions.</span></span>

### <span data-ttu-id="4bb8b-116">Przykład 3. Generowanie tokenu podpisu dostępu udostępnionego, który korzysta z zasad dostępu udostępnionego</span><span class="sxs-lookup"><span data-stu-id="4bb8b-116">Example 3: Generate a shared access signature token that uses a shared access policy</span></span>
```
PS C:\>New-AzStorageShareSASToken -ShareName "ContosoShare" -Policy "ContosoPolicy03"
```

<span data-ttu-id="4bb8b-117">To polecenie tworzy token podpisu dostępu udostępnionego dla udziału magazynu o nazwie ContosoShare, który ma zasady o nazwie ContosoPolicy03.</span><span class="sxs-lookup"><span data-stu-id="4bb8b-117">This command creates a shared access signature token for the Storage share named ContosoShare that has the policy named ContosoPolicy03.</span></span>

## <span data-ttu-id="4bb8b-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4bb8b-118">PARAMETERS</span></span>

### <span data-ttu-id="4bb8b-119">— kontekst</span><span class="sxs-lookup"><span data-stu-id="4bb8b-119">-Context</span></span>
<span data-ttu-id="4bb8b-120">Określa kontekst magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="4bb8b-120">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="4bb8b-121">Aby uzyskać kontekst, użyj polecenia cmdlet New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4bb8b-121">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4bb8b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bb8b-122">-DefaultProfile</span></span>
<span data-ttu-id="4bb8b-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="4bb8b-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4bb8b-124">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="4bb8b-124">-ExpiryTime</span></span>
<span data-ttu-id="4bb8b-125">Określa czas, w którym podpis dostępu udostępnionego staje się nieprawidłowy.</span><span class="sxs-lookup"><span data-stu-id="4bb8b-125">Specifies the time at which the shared access signature becomes invalid.</span></span>

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

### <span data-ttu-id="4bb8b-126">-FullUri</span><span class="sxs-lookup"><span data-stu-id="4bb8b-126">-FullUri</span></span>
<span data-ttu-id="4bb8b-127">Wskazuje, że to polecenie cmdlet zwraca pełny adres URI obiektu blob i token podpisu dostępu udostępnionego.</span><span class="sxs-lookup"><span data-stu-id="4bb8b-127">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="4bb8b-128">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="4bb8b-128">-IPAddressOrRange</span></span>
<span data-ttu-id="4bb8b-129">Określa adres IP lub zakres adresów IP, z których mają być akceptowane żądania, na przykład 168.1.5.65 lub 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="4bb8b-129">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="4bb8b-130">Zakres jest włącznie.</span><span class="sxs-lookup"><span data-stu-id="4bb8b-130">The range is inclusive.</span></span>

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

### <span data-ttu-id="4bb8b-131">— Uprawnienie</span><span class="sxs-lookup"><span data-stu-id="4bb8b-131">-Permission</span></span>
<span data-ttu-id="4bb8b-132">Określa uprawnienia w tokenie do uzyskiwania dostępu do udziału i plików w ramach udziału.</span><span class="sxs-lookup"><span data-stu-id="4bb8b-132">Specifies the permissions in the token to access the share and files under the share.</span></span>
<span data-ttu-id="4bb8b-133">Należy pamiętać, że jest to ciąg, taki jak `rwd` (w przypadku odczytu, zapisu i usunięcia).</span><span class="sxs-lookup"><span data-stu-id="4bb8b-133">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

```yaml
Type: System.String
Parameter Sets: SasPermission
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bb8b-134">— Zasady</span><span class="sxs-lookup"><span data-stu-id="4bb8b-134">-Policy</span></span>
<span data-ttu-id="4bb8b-135">Określa przechowywane zasady dostępu dla udziału.</span><span class="sxs-lookup"><span data-stu-id="4bb8b-135">Specifies the stored access policy for a share.</span></span>

```yaml
Type: System.String
Parameter Sets: SasPolicy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bb8b-136">— Protokół</span><span class="sxs-lookup"><span data-stu-id="4bb8b-136">-Protocol</span></span>
<span data-ttu-id="4bb8b-137">Określa protokół dozwolony dla żądania.</span><span class="sxs-lookup"><span data-stu-id="4bb8b-137">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="4bb8b-138">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="4bb8b-138">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="4bb8b-139">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="4bb8b-139">HttpsOnly</span></span>
* <span data-ttu-id="4bb8b-140">HttpsOrHttp Wartość domyślna to httpsorhttp.</span><span class="sxs-lookup"><span data-stu-id="4bb8b-140">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="4bb8b-141">-ShareName</span><span class="sxs-lookup"><span data-stu-id="4bb8b-141">-ShareName</span></span>
<span data-ttu-id="4bb8b-142">Określa nazwę udziału magazynu.</span><span class="sxs-lookup"><span data-stu-id="4bb8b-142">Specifies the name of the Storage share.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4bb8b-143">— StartTime</span><span class="sxs-lookup"><span data-stu-id="4bb8b-143">-StartTime</span></span>
<span data-ttu-id="4bb8b-144">Określa czas, w którym podpis dostępu udostępnionego stanie się prawidłowy.</span><span class="sxs-lookup"><span data-stu-id="4bb8b-144">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="4bb8b-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bb8b-145">CommonParameters</span></span>
<span data-ttu-id="4bb8b-146">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4bb8b-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bb8b-147">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4bb8b-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bb8b-148">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4bb8b-148">INPUTS</span></span>

### <span data-ttu-id="4bb8b-149">System.String</span><span class="sxs-lookup"><span data-stu-id="4bb8b-149">System.String</span></span>

### <span data-ttu-id="4bb8b-150">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="4bb8b-150">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="4bb8b-151">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4bb8b-151">OUTPUTS</span></span>

### <span data-ttu-id="4bb8b-152">System.String</span><span class="sxs-lookup"><span data-stu-id="4bb8b-152">System.String</span></span>

## <span data-ttu-id="4bb8b-153">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4bb8b-153">NOTES</span></span>
* <span data-ttu-id="4bb8b-154">Słowa kluczowe: common, azure, services, data, storage, blob, queue, table</span><span class="sxs-lookup"><span data-stu-id="4bb8b-154">Keywords: common, azure, services, data, storage, blob, queue, table</span></span>

## <span data-ttu-id="4bb8b-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4bb8b-155">RELATED LINKS</span></span>

[<span data-ttu-id="4bb8b-156">Get-AzstorageShare</span><span class="sxs-lookup"><span data-stu-id="4bb8b-156">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="4bb8b-157">New-azstorageFilesasToken</span><span class="sxs-lookup"><span data-stu-id="4bb8b-157">New-AzStorageFileSASToken</span></span>](./New-AzStorageFileSASToken.md)
