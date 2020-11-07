---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: BCCBB05B-A5D7-4796-BE55-6BE5E18E07FC
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageaccountsastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountSASToken.md
ms.openlocfilehash: 83480321e58d4dbd21d0a13dd6139c2f2d905c33
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93888069"
---
# <span data-ttu-id="9e944-101">New-AzStorageAccountSASToken</span><span class="sxs-lookup"><span data-stu-id="9e944-101">New-AzStorageAccountSASToken</span></span>

## <span data-ttu-id="9e944-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9e944-102">SYNOPSIS</span></span>
<span data-ttu-id="9e944-103">Umożliwia utworzenie tokenu SAS na poziomie konta.</span><span class="sxs-lookup"><span data-stu-id="9e944-103">Creates an account-level SAS token.</span></span>

## <span data-ttu-id="9e944-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9e944-104">SYNTAX</span></span>

```
New-AzStorageAccountSASToken -Service <SharedAccessAccountServices>
 -ResourceType <SharedAccessAccountResourceTypes> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9e944-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9e944-105">DESCRIPTION</span></span>
<span data-ttu-id="9e944-106">Polecenie cmdlet **New-AzStorageSASToken** umożliwia utworzenie tokenu SAS (Shared Access Signature) na poziomie konta dla konta usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="9e944-106">The **New-AzStorageSASToken** cmdlet creates an account-level shared access signature (SAS) token for an Azure Storage account.</span></span>
<span data-ttu-id="9e944-107">Tokena SAS można używać do delegowania uprawnień dla wielu usług lub do delegowania uprawnień dla usług niedostępnych z tokenem SAS na poziomie obiektu.</span><span class="sxs-lookup"><span data-stu-id="9e944-107">You can use the SAS token to delegate permissions for multiple services, or to delegate permissions for services not available with an object-level SAS token.</span></span>

## <span data-ttu-id="9e944-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9e944-108">EXAMPLES</span></span>

### <span data-ttu-id="9e944-109">Przykład 1. Tworzenie tokenu SAS na poziomie konta z pełnymi uprawnieniami</span><span class="sxs-lookup"><span data-stu-id="9e944-109">Example 1: Create an account-level SAS token with full permission</span></span>
```
PS C:\> New-AzStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup"
```

<span data-ttu-id="9e944-110">To polecenie tworzy token SAS na poziomie konta z pełnymi uprawnieniami.</span><span class="sxs-lookup"><span data-stu-id="9e944-110">This command creates an account-level SAS token with full permission.</span></span>

### <span data-ttu-id="9e944-111">Przykład 2: Tworzenie tokenu SAS na poziomie konta dla zakresu adresów IP</span><span class="sxs-lookup"><span data-stu-id="9e944-111">Example 2: Create an account-level SAS token for a range of IP addresses</span></span>
```
PS C:\> New-AzStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup" -Protocol HttpsOnly -IPAddressOrRange 168.1.5.60-168.1.5.70
```

<span data-ttu-id="9e944-112">To polecenie tworzy token SAS na poziomie konta dla żądań dotyczących tylko HTTPS z określonego zakresu adresów IP.</span><span class="sxs-lookup"><span data-stu-id="9e944-112">This command creates an account-level SAS token for HTTPS-only requests from the specified range of IP addresses.</span></span>

## <span data-ttu-id="9e944-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9e944-113">PARAMETERS</span></span>

### <span data-ttu-id="9e944-114">-Context</span><span class="sxs-lookup"><span data-stu-id="9e944-114">-Context</span></span>
<span data-ttu-id="9e944-115">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="9e944-115">Specifies the Azure storage context.</span></span>
<span data-ttu-id="9e944-116">Możesz użyć polecenia cmdlet New-AzStorageContext, aby uzyskać obiekt **AzureStorageContext** .</span><span class="sxs-lookup"><span data-stu-id="9e944-116">You can use the New-AzStorageContext cmdlet to get an **AzureStorageContext** object.</span></span>

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

### <span data-ttu-id="9e944-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e944-117">-DefaultProfile</span></span>
<span data-ttu-id="9e944-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9e944-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e944-119">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="9e944-119">-ExpiryTime</span></span>
<span data-ttu-id="9e944-120">Określa czas, po upływie którego podpis udostępniony jest nieprawidłowy.</span><span class="sxs-lookup"><span data-stu-id="9e944-120">Specifies the time at which the shared access signature becomes invalid.</span></span>

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

### <span data-ttu-id="9e944-121">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="9e944-121">-IPAddressOrRange</span></span>
<span data-ttu-id="9e944-122">Określa adres IP lub zakres adresów IP, od których należy akceptować żądania, takie jak 168.1.5.65 lub 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="9e944-122">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="9e944-123">Zakresem jest włącznie.</span><span class="sxs-lookup"><span data-stu-id="9e944-123">The range is inclusive.</span></span>

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

### <span data-ttu-id="9e944-124">-Uprawnienie</span><span class="sxs-lookup"><span data-stu-id="9e944-124">-Permission</span></span>
<span data-ttu-id="9e944-125">Określa uprawnienia do konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="9e944-125">Specifies the permissions for Storage account.</span></span>
<span data-ttu-id="9e944-126">Uprawnienia są ważne tylko wtedy, gdy pasują do określonego typu zasobu.</span><span class="sxs-lookup"><span data-stu-id="9e944-126">Permissions are valid only if they match the specified resource type.</span></span>
<span data-ttu-id="9e944-127">Ważne jest, aby zwrócić uwagę, że jest to ciąg, taki jak `rwd` (na przykład odczyt, zapis i usuwanie).</span><span class="sxs-lookup"><span data-stu-id="9e944-127">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>
<span data-ttu-id="9e944-128">Aby uzyskać więcej informacji na temat dopuszczalnych wartości uprawnień, zobacz konstruowanie skojarzeń zabezpieczeń konta https://go.microsoft.com/fwlink/?LinkId=799514</span><span class="sxs-lookup"><span data-stu-id="9e944-128">For more information about acceptable permission values, see Constructing an Account SAS https://go.microsoft.com/fwlink/?LinkId=799514</span></span>

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

### <span data-ttu-id="9e944-129">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="9e944-129">-Protocol</span></span>
<span data-ttu-id="9e944-130">Umożliwia określenie protokołu dozwolonego dla żądania wykonywanego za pomocą skojarzeń zabezpieczeń konta.</span><span class="sxs-lookup"><span data-stu-id="9e944-130">Specifies the protocol permitted for a request made with the account SAS.</span></span>
<span data-ttu-id="9e944-131">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="9e944-131">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9e944-132">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="9e944-132">HttpsOnly</span></span>
- <span data-ttu-id="9e944-133">HttpsOrHttp wartość domyślna to HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="9e944-133">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="9e944-134">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="9e944-134">-ResourceType</span></span>
<span data-ttu-id="9e944-135">Określa typy zasobów dostępne w tokenie SAS.</span><span class="sxs-lookup"><span data-stu-id="9e944-135">Specifies the resource types that are available with the SAS token.</span></span>
<span data-ttu-id="9e944-136">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="9e944-136">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9e944-137">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="9e944-137">None</span></span>
- <span data-ttu-id="9e944-138">Służby</span><span class="sxs-lookup"><span data-stu-id="9e944-138">Service</span></span>
- <span data-ttu-id="9e944-139">Opakowaniu</span><span class="sxs-lookup"><span data-stu-id="9e944-139">Container</span></span>
- <span data-ttu-id="9e944-140">Stream</span><span class="sxs-lookup"><span data-stu-id="9e944-140">Object</span></span>

```yaml
Type: Microsoft.Azure.Storage.SharedAccessAccountResourceTypes
Parameter Sets: (All)
Aliases:
Accepted values: None, Service, Container, Object

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e944-141">-Service</span><span class="sxs-lookup"><span data-stu-id="9e944-141">-Service</span></span>
<span data-ttu-id="9e944-142">Określa usługę.</span><span class="sxs-lookup"><span data-stu-id="9e944-142">Specifies the service.</span></span>
<span data-ttu-id="9e944-143">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="9e944-143">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9e944-144">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="9e944-144">None</span></span>
- <span data-ttu-id="9e944-145">Obiektów BLOB</span><span class="sxs-lookup"><span data-stu-id="9e944-145">Blob</span></span>
- <span data-ttu-id="9e944-146">Plik</span><span class="sxs-lookup"><span data-stu-id="9e944-146">File</span></span>
- <span data-ttu-id="9e944-147">Wykonany</span><span class="sxs-lookup"><span data-stu-id="9e944-147">Queue</span></span>
- <span data-ttu-id="9e944-148">Tworząc</span><span class="sxs-lookup"><span data-stu-id="9e944-148">Table</span></span>

```yaml
Type: Microsoft.Azure.Storage.SharedAccessAccountServices
Parameter Sets: (All)
Aliases:
Accepted values: None, Blob, File, Queue, Table

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e944-149">-StartTime</span><span class="sxs-lookup"><span data-stu-id="9e944-149">-StartTime</span></span>
<span data-ttu-id="9e944-150">Określa czas (w postaci obiektu **DateTime** ), po upływie którego te skojarzenia będą obowiązywać.</span><span class="sxs-lookup"><span data-stu-id="9e944-150">Specifies the time, as a **DateTime** object, at which the SAS becomes valid.</span></span>
<span data-ttu-id="9e944-151">Aby uzyskać obiekt **DateTime** , użyj polecenia cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="9e944-151">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="9e944-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e944-152">CommonParameters</span></span>
<span data-ttu-id="9e944-153">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e944-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e944-154">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e944-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e944-155">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9e944-155">INPUTS</span></span>

### <span data-ttu-id="9e944-156">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="9e944-156">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="9e944-157">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9e944-157">OUTPUTS</span></span>

### <span data-ttu-id="9e944-158">System. String</span><span class="sxs-lookup"><span data-stu-id="9e944-158">System.String</span></span>

## <span data-ttu-id="9e944-159">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9e944-159">NOTES</span></span>

## <span data-ttu-id="9e944-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9e944-160">RELATED LINKS</span></span>

[<span data-ttu-id="9e944-161">Nowe — AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="9e944-161">New-AzStorageBlobSASToken</span></span>](./New-AzStorageBlobSASToken.md)

[<span data-ttu-id="9e944-162">Nowe — AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="9e944-162">New-AzStorageContainerSASToken</span></span>](./New-AzStorageContainerSASToken.md)

[<span data-ttu-id="9e944-163">Nowe — AzStorageFileSASToken</span><span class="sxs-lookup"><span data-stu-id="9e944-163">New-AzStorageFileSASToken</span></span>](./New-AzStorageFileSASToken.md)

[<span data-ttu-id="9e944-164">Nowe — AzStorageQueueSASToken</span><span class="sxs-lookup"><span data-stu-id="9e944-164">New-AzStorageQueueSASToken</span></span>](./New-AzStorageQueueSASToken.md)

[<span data-ttu-id="9e944-165">Nowe — AzStorageShareSASToken</span><span class="sxs-lookup"><span data-stu-id="9e944-165">New-AzStorageShareSASToken</span></span>](./New-AzStorageShareSASToken.md)

[<span data-ttu-id="9e944-166">Nowe — AzStorageTableSASToken</span><span class="sxs-lookup"><span data-stu-id="9e944-166">New-AzStorageTableSASToken</span></span>](./New-AzStorageTableSASToken.md)


