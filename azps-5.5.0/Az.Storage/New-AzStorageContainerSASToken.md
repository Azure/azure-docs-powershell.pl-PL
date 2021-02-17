---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 6FF04E82-4921-4F7B-83D0-6997316BC5FD
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragecontainersastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainerSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainerSASToken.md
ms.openlocfilehash: 4e265fab8df3abd897c27131e0673241ce37b946
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198426"
---
# <span data-ttu-id="d18a9-101">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="d18a9-101">New-AzStorageContainerSASToken</span></span>

## <span data-ttu-id="d18a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d18a9-102">SYNOPSIS</span></span>
<span data-ttu-id="d18a9-103">Generuje token SAS dla kontenera magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d18a9-103">Generates an SAS token for an Azure storage container.</span></span>

## <span data-ttu-id="d18a9-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d18a9-104">SYNTAX</span></span>

### <span data-ttu-id="d18a9-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="d18a9-105">SasPolicy</span></span>
```
New-AzStorageContainerSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d18a9-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="d18a9-106">SasPermission</span></span>
```
New-AzStorageContainerSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d18a9-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="d18a9-107">DESCRIPTION</span></span>
<span data-ttu-id="d18a9-108">Polecenie cmdlet **New-AzStorageContainerSASToken** generuje token SAS (Shared Access Signature) dla kontenera magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d18a9-108">The **New-AzStorageContainerSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure storage container.</span></span>

## <span data-ttu-id="d18a9-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d18a9-109">EXAMPLES</span></span>

### <span data-ttu-id="d18a9-110">Przykład 1. Generowanie tokenu SAS kontenera z pełnymi uprawnieniami kontenera</span><span class="sxs-lookup"><span data-stu-id="d18a9-110">Example 1: Generate a container SAS token with full container permission</span></span>
```
PS C:\>New-AzStorageContainerSASToken -Name "Test" -Permission rwdl
```

<span data-ttu-id="d18a9-111">W tym przykładzie jest generowany token SAS kontenera z pełnymi uprawnieniami kontenera.</span><span class="sxs-lookup"><span data-stu-id="d18a9-111">This example generates a container SAS token with full container permission.</span></span>

### <span data-ttu-id="d18a9-112">Przykład 2. Generowanie wielu kontenerów tokenu SAS według potoku</span><span class="sxs-lookup"><span data-stu-id="d18a9-112">Example 2: Generate multiple container SAS token by pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -Container test* | New-AzStorageContainerSASToken -Permission rwdl
```

<span data-ttu-id="d18a9-113">W tym przykładzie jest generowanych wiele tokenów SAS kontenera przy użyciu potoku.</span><span class="sxs-lookup"><span data-stu-id="d18a9-113">This example generates multiple container SAS tokens by using the pipeline.</span></span>

### <span data-ttu-id="d18a9-114">Przykład 3. Generowanie tokenu SAS kontenera za pomocą zasad dostępu udostępnionego</span><span class="sxs-lookup"><span data-stu-id="d18a9-114">Example 3: Generate container SAS token with shared access policy</span></span>
```
PS C:\>New-AzStorageContainerSASToken -Name "Test" -Policy "PolicyName"
```

<span data-ttu-id="d18a9-115">W tym przykładzie jest generowany token SAS kontenera z zasadami dostępu udostępnionego.</span><span class="sxs-lookup"><span data-stu-id="d18a9-115">This example generates a container SAS token with shared access policy.</span></span>

### <span data-ttu-id="d18a9-116">Przykład 3. Generowanie tokenu SAS kontenera tożsamości użytkownika z kontekstem magazynowania na podstawie uwierzytelniania OAuth</span><span class="sxs-lookup"><span data-stu-id="d18a9-116">Example 3: Generate a User Identity container SAS token with storage context based on OAuth authentication</span></span>
```
PS C:\> $ctx = New-AzStorageContext -StorageAccountName $accountName -UseConnectedAccount
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $startTime.AddDays(6)
PS C:\> New-AzStorageContainerSASToken -Name "ContainerName" -Permission rwd -StartTime $StartTime -ExpiryTime $EndTime -context $ctx
```

<span data-ttu-id="d18a9-117">W tym przykładzie jest generowany token SAS kontenera tożsamości użytkownika z kontekstem magazynowania na podstawie uwierzytelniania OAuth</span><span class="sxs-lookup"><span data-stu-id="d18a9-117">This example generates a User Identity container SAS token with storage context based on OAuth authentication</span></span>

## <span data-ttu-id="d18a9-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d18a9-118">PARAMETERS</span></span>

### <span data-ttu-id="d18a9-119">— kontekst</span><span class="sxs-lookup"><span data-stu-id="d18a9-119">-Context</span></span>
<span data-ttu-id="d18a9-120">Określa kontekst magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d18a9-120">Specifies an Azure storage context.</span></span>
<span data-ttu-id="d18a9-121">Możesz go utworzyć za pomocą polecenia cmdlet New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d18a9-121">You can create it by using the New-AzStorageContext cmdlet.</span></span>
<span data-ttu-id="d18a9-122">Gdy kontekst magazynu jest oparty na uwierzytelnieniu OAuth, wygeneruje token SAS kontenera tożsamości użytkownika.</span><span class="sxs-lookup"><span data-stu-id="d18a9-122">When the storage context is based on OAuth authentication, will generates a User Identity container SAS token.</span></span>

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

### <span data-ttu-id="d18a9-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d18a9-123">-DefaultProfile</span></span>
<span data-ttu-id="d18a9-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d18a9-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d18a9-125">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="d18a9-125">-ExpiryTime</span></span>
<span data-ttu-id="d18a9-126">Określa czas, w którym podpis dostępu udostępnionego staje się nieprawidłowy.</span><span class="sxs-lookup"><span data-stu-id="d18a9-126">Specifies the time at which the shared access signature becomes invalid.</span></span>
<span data-ttu-id="d18a9-127">Jeśli użytkownik ustawi godzinę rozpoczęcia, ale nie czas wygaśnięcia, czas wygaśnięcia zostanie ustawiony na godzinę rozpoczęcia plus godzina.</span><span class="sxs-lookup"><span data-stu-id="d18a9-127">If the user sets the start time but not the expiry time, the expiry time is set to the start time plus one hour.</span></span>
<span data-ttu-id="d18a9-128">Jeśli ani godzina rozpoczęcia, ani czas wygaśnięcia nie są określone, czas wygaśnięcia jest ustawiany na bieżący czas plus godzina.</span><span class="sxs-lookup"><span data-stu-id="d18a9-128">If neither the start time nor the expiry time is specified, the expiry time is set to the current time plus one hour.</span></span>
<span data-ttu-id="d18a9-129">Jeśli kontekst magazynu jest oparty na uwierzytelnianiu OAuth, czas wygaśnięcia musi upłynąć 7 dni od bieżącej godziny i nie może być wcześniejszy niż bieżący czas.</span><span class="sxs-lookup"><span data-stu-id="d18a9-129">When the storage context is based on OAuth authentication, the expire time must be in 7 days from current time, and must not be earlier than current time.</span></span>

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

### <span data-ttu-id="d18a9-130">-FullUri</span><span class="sxs-lookup"><span data-stu-id="d18a9-130">-FullUri</span></span>
<span data-ttu-id="d18a9-131">Wskazuje, że to polecenie cmdlet zwraca pełny adres URI obiektu blob i token podpisu dostępu udostępnionego.</span><span class="sxs-lookup"><span data-stu-id="d18a9-131">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="d18a9-132">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="d18a9-132">-IPAddressOrRange</span></span>
<span data-ttu-id="d18a9-133">Określa adres IP lub zakres adresów IP, z których mają być akceptowane żądania, na przykład 168.1.5.65 lub 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="d18a9-133">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="d18a9-134">Zakres jest włącznie.</span><span class="sxs-lookup"><span data-stu-id="d18a9-134">The range is inclusive.</span></span>

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

### <span data-ttu-id="d18a9-135">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d18a9-135">-Name</span></span>
<span data-ttu-id="d18a9-136">Określa nazwę kontenera magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d18a9-136">Specifies an Azure storage container name.</span></span>

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

### <span data-ttu-id="d18a9-137">— Uprawnienie</span><span class="sxs-lookup"><span data-stu-id="d18a9-137">-Permission</span></span>
<span data-ttu-id="d18a9-138">Określa uprawnienia dla kontenera magazynu.</span><span class="sxs-lookup"><span data-stu-id="d18a9-138">Specifies permissions for a storage container.</span></span>
<span data-ttu-id="d18a9-139">Należy pamiętać, że jest to ciąg, taki jak `rwd` (w przypadku odczytu, zapisu i usunięcia).</span><span class="sxs-lookup"><span data-stu-id="d18a9-139">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="d18a9-140">— Zasady</span><span class="sxs-lookup"><span data-stu-id="d18a9-140">-Policy</span></span>
<span data-ttu-id="d18a9-141">Określa zasady przechowywanego dostępu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d18a9-141">Specifies an Azure Stored Access Policy.</span></span>

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

### <span data-ttu-id="d18a9-142">— Protokół</span><span class="sxs-lookup"><span data-stu-id="d18a9-142">-Protocol</span></span>
<span data-ttu-id="d18a9-143">Określa protokół dozwolony dla żądania.</span><span class="sxs-lookup"><span data-stu-id="d18a9-143">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="d18a9-144">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="d18a9-144">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="d18a9-145">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="d18a9-145">HttpsOnly</span></span>
* <span data-ttu-id="d18a9-146">HttpsOrHttp Wartość domyślna to httpsorhttp.</span><span class="sxs-lookup"><span data-stu-id="d18a9-146">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="d18a9-147">— StartTime</span><span class="sxs-lookup"><span data-stu-id="d18a9-147">-StartTime</span></span>
<span data-ttu-id="d18a9-148">Określa czas, w którym podpis dostępu udostępnionego stanie się prawidłowy.</span><span class="sxs-lookup"><span data-stu-id="d18a9-148">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="d18a9-149">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d18a9-149">-Confirm</span></span>
<span data-ttu-id="d18a9-150">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d18a9-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d18a9-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d18a9-151">-WhatIf</span></span>
<span data-ttu-id="d18a9-152">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d18a9-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d18a9-153">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d18a9-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d18a9-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d18a9-154">CommonParameters</span></span>
<span data-ttu-id="d18a9-155">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d18a9-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d18a9-156">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d18a9-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d18a9-157">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d18a9-157">INPUTS</span></span>

### <span data-ttu-id="d18a9-158">System.String</span><span class="sxs-lookup"><span data-stu-id="d18a9-158">System.String</span></span>

### <span data-ttu-id="d18a9-159">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="d18a9-159">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="d18a9-160">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d18a9-160">OUTPUTS</span></span>

### <span data-ttu-id="d18a9-161">System.String</span><span class="sxs-lookup"><span data-stu-id="d18a9-161">System.String</span></span>

## <span data-ttu-id="d18a9-162">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d18a9-162">NOTES</span></span>

## <span data-ttu-id="d18a9-163">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d18a9-163">RELATED LINKS</span></span>

[<span data-ttu-id="d18a9-164">New-AzstorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="d18a9-164">New-AzStorageBlobSASToken</span></span>](./New-AzStorageBlobSASToken.md)
