---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 6FF04E82-4921-4F7B-83D0-6997316BC5FD
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragecontainersastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainerSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainerSASToken.md
ms.openlocfilehash: 4e265fab8df3abd897c27131e0673241ce37b946
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98374031"
---
# <span data-ttu-id="b5482-101">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="b5482-101">New-AzStorageContainerSASToken</span></span>

## <span data-ttu-id="b5482-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b5482-102">SYNOPSIS</span></span>
<span data-ttu-id="b5482-103">Generuje token SAS dla kontenera magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b5482-103">Generates an SAS token for an Azure storage container.</span></span>

## <span data-ttu-id="b5482-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b5482-104">SYNTAX</span></span>

### <span data-ttu-id="b5482-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="b5482-105">SasPolicy</span></span>
```
New-AzStorageContainerSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b5482-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="b5482-106">SasPermission</span></span>
```
New-AzStorageContainerSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b5482-107">Opis</span><span class="sxs-lookup"><span data-stu-id="b5482-107">DESCRIPTION</span></span>
<span data-ttu-id="b5482-108">Polecenie cmdlet **New-AzStorageContainerSASToken** generuje token dostępu współużytkowanego (SAS) dla kontenera magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b5482-108">The **New-AzStorageContainerSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure storage container.</span></span>

## <span data-ttu-id="b5482-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b5482-109">EXAMPLES</span></span>

### <span data-ttu-id="b5482-110">Przykład 1. Generuj token SAS kontenera z uprawnieniem pełny kontener</span><span class="sxs-lookup"><span data-stu-id="b5482-110">Example 1: Generate a container SAS token with full container permission</span></span>
```
PS C:\>New-AzStorageContainerSASToken -Name "Test" -Permission rwdl
```

<span data-ttu-id="b5482-111">W tym przykładzie Wygenerowano token SAS kontenera z uprawnieniem pełnego kontenera.</span><span class="sxs-lookup"><span data-stu-id="b5482-111">This example generates a container SAS token with full container permission.</span></span>

### <span data-ttu-id="b5482-112">Przykład 2: generowanie wielu tokenów SAS kontenera według rurociągu</span><span class="sxs-lookup"><span data-stu-id="b5482-112">Example 2: Generate multiple container SAS token by pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -Container test* | New-AzStorageContainerSASToken -Permission rwdl
```

<span data-ttu-id="b5482-113">W tym przykładzie Wygenerowano wiele tokenów SAS kontenera za pomocą potoku.</span><span class="sxs-lookup"><span data-stu-id="b5482-113">This example generates multiple container SAS tokens by using the pipeline.</span></span>

### <span data-ttu-id="b5482-114">Przykład 3: generowanie tokenu SAS kontenera z zasadami dostępu współużytkowanego</span><span class="sxs-lookup"><span data-stu-id="b5482-114">Example 3: Generate container SAS token with shared access policy</span></span>
```
PS C:\>New-AzStorageContainerSASToken -Name "Test" -Policy "PolicyName"
```

<span data-ttu-id="b5482-115">W tym przykładzie Wygenerowano token SAS kontenera z zasadami dostępu współużytkowanego.</span><span class="sxs-lookup"><span data-stu-id="b5482-115">This example generates a container SAS token with shared access policy.</span></span>

### <span data-ttu-id="b5482-116">Przykład 3: generowanie tokenu SAS kontenera tożsamości użytkownika z kontekstem magazynu na podstawie uwierzytelniania OAuth</span><span class="sxs-lookup"><span data-stu-id="b5482-116">Example 3: Generate a User Identity container SAS token with storage context based on OAuth authentication</span></span>
```
PS C:\> $ctx = New-AzStorageContext -StorageAccountName $accountName -UseConnectedAccount
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $startTime.AddDays(6)
PS C:\> New-AzStorageContainerSASToken -Name "ContainerName" -Permission rwd -StartTime $StartTime -ExpiryTime $EndTime -context $ctx
```

<span data-ttu-id="b5482-117">W tym przykładzie Wygenerowano token SAS kontenera tożsamości użytkownika z kontekstem magazynu na podstawie uwierzytelniania OAuth</span><span class="sxs-lookup"><span data-stu-id="b5482-117">This example generates a User Identity container SAS token with storage context based on OAuth authentication</span></span>

## <span data-ttu-id="b5482-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b5482-118">PARAMETERS</span></span>

### <span data-ttu-id="b5482-119">-Context</span><span class="sxs-lookup"><span data-stu-id="b5482-119">-Context</span></span>
<span data-ttu-id="b5482-120">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="b5482-120">Specifies an Azure storage context.</span></span>
<span data-ttu-id="b5482-121">Możesz ją utworzyć przy użyciu polecenia cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="b5482-121">You can create it by using the New-AzStorageContext cmdlet.</span></span>
<span data-ttu-id="b5482-122">Gdy kontekst magazynu jest oparty na uwierzytelnianiu OAuth, zostanie wygenerowany token SAS kontenera tożsamości użytkownika.</span><span class="sxs-lookup"><span data-stu-id="b5482-122">When the storage context is based on OAuth authentication, will generates a User Identity container SAS token.</span></span>

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

### <span data-ttu-id="b5482-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5482-123">-DefaultProfile</span></span>
<span data-ttu-id="b5482-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b5482-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5482-125">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="b5482-125">-ExpiryTime</span></span>
<span data-ttu-id="b5482-126">Określa czas, po upływie którego podpis udostępniony jest nieprawidłowy.</span><span class="sxs-lookup"><span data-stu-id="b5482-126">Specifies the time at which the shared access signature becomes invalid.</span></span>
<span data-ttu-id="b5482-127">Jeśli użytkownik ustawi czas rozpoczęcia, ale nie czas wygaśnięcia, czas wygaśnięcia jest ustawiany na czas rozpoczęcia Plus o godzinę.</span><span class="sxs-lookup"><span data-stu-id="b5482-127">If the user sets the start time but not the expiry time, the expiry time is set to the start time plus one hour.</span></span>
<span data-ttu-id="b5482-128">Jeśli nie określono godziny rozpoczęcia ani godziny wygaśnięcia, czas wygaśnięcia jest ustawiany na bieżący czas plus co godzinę.</span><span class="sxs-lookup"><span data-stu-id="b5482-128">If neither the start time nor the expiry time is specified, the expiry time is set to the current time plus one hour.</span></span>
<span data-ttu-id="b5482-129">Gdy kontekst magazynu jest oparty na uwierzytelnianiu OAuth, czas wygaśnięcia musi wynosić w ciągu 7 dni od bieżącego czasu i nie może być wcześniejszy niż bieżący czas.</span><span class="sxs-lookup"><span data-stu-id="b5482-129">When the storage context is based on OAuth authentication, the expire time must be in 7 days from current time, and must not be earlier than current time.</span></span>

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

### <span data-ttu-id="b5482-130">-FullUri</span><span class="sxs-lookup"><span data-stu-id="b5482-130">-FullUri</span></span>
<span data-ttu-id="b5482-131">Wskazuje, że to polecenie cmdlet zwróci pełny identyfikator URI obiektu BLOB i token podpisu dostępu współdzielonego.</span><span class="sxs-lookup"><span data-stu-id="b5482-131">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="b5482-132">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="b5482-132">-IPAddressOrRange</span></span>
<span data-ttu-id="b5482-133">Określa adres IP lub zakres adresów IP, od których należy akceptować żądania, takie jak 168.1.5.65 lub 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="b5482-133">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="b5482-134">Zakresem jest włącznie.</span><span class="sxs-lookup"><span data-stu-id="b5482-134">The range is inclusive.</span></span>

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

### <span data-ttu-id="b5482-135">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b5482-135">-Name</span></span>
<span data-ttu-id="b5482-136">Określa nazwę kontenera magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b5482-136">Specifies an Azure storage container name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Container

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b5482-137">-Uprawnienie</span><span class="sxs-lookup"><span data-stu-id="b5482-137">-Permission</span></span>
<span data-ttu-id="b5482-138">Określa uprawnienia kontenera magazynu.</span><span class="sxs-lookup"><span data-stu-id="b5482-138">Specifies permissions for a storage container.</span></span>
<span data-ttu-id="b5482-139">Ważne jest, aby zwrócić uwagę, że jest to ciąg, taki jak `rwd` (na przykład odczyt, zapis i usuwanie).</span><span class="sxs-lookup"><span data-stu-id="b5482-139">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="b5482-140">-Policy</span><span class="sxs-lookup"><span data-stu-id="b5482-140">-Policy</span></span>
<span data-ttu-id="b5482-141">Określa zasady dostępu przechowywane na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="b5482-141">Specifies an Azure Stored Access Policy.</span></span>

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

### <span data-ttu-id="b5482-142">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="b5482-142">-Protocol</span></span>
<span data-ttu-id="b5482-143">Określa protokół dozwolony dla żądania.</span><span class="sxs-lookup"><span data-stu-id="b5482-143">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="b5482-144">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="b5482-144">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="b5482-145">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="b5482-145">HttpsOnly</span></span>
* <span data-ttu-id="b5482-146">HttpsOrHttp wartość domyślna to HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="b5482-146">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="b5482-147">-StartTime</span><span class="sxs-lookup"><span data-stu-id="b5482-147">-StartTime</span></span>
<span data-ttu-id="b5482-148">Określa czas, po upływie którego podpis udostępniony będzie ważny.</span><span class="sxs-lookup"><span data-stu-id="b5482-148">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="b5482-149">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b5482-149">-Confirm</span></span>
<span data-ttu-id="b5482-150">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5482-150">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5482-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5482-151">-WhatIf</span></span>
<span data-ttu-id="b5482-152">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5482-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b5482-153">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b5482-153">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5482-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5482-154">CommonParameters</span></span>
<span data-ttu-id="b5482-155">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5482-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5482-156">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5482-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5482-157">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b5482-157">INPUTS</span></span>

### <span data-ttu-id="b5482-158">System. String</span><span class="sxs-lookup"><span data-stu-id="b5482-158">System.String</span></span>

### <span data-ttu-id="b5482-159">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="b5482-159">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="b5482-160">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b5482-160">OUTPUTS</span></span>

### <span data-ttu-id="b5482-161">System. String</span><span class="sxs-lookup"><span data-stu-id="b5482-161">System.String</span></span>

## <span data-ttu-id="b5482-162">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b5482-162">NOTES</span></span>

## <span data-ttu-id="b5482-163">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b5482-163">RELATED LINKS</span></span>

[<span data-ttu-id="b5482-164">Nowe — AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="b5482-164">New-AzStorageBlobSASToken</span></span>](./New-AzStorageBlobSASToken.md)
