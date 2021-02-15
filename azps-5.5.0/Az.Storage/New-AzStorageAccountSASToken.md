---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: BCCBB05B-A5D7-4796-BE55-6BE5E18E07FC
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageaccountsastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountSASToken.md
ms.openlocfilehash: 3c79266c6f6e9b5200e2224f463ac12fe409bf0c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195746"
---
# <span data-ttu-id="b7b3b-101">New-AzStorageAccountSASToken</span><span class="sxs-lookup"><span data-stu-id="b7b3b-101">New-AzStorageAccountSASToken</span></span>

## <span data-ttu-id="b7b3b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7b3b-102">SYNOPSIS</span></span>
<span data-ttu-id="b7b3b-103">Tworzy token SAS na poziomie konta.</span><span class="sxs-lookup"><span data-stu-id="b7b3b-103">Creates an account-level SAS token.</span></span>

## <span data-ttu-id="b7b3b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b7b3b-104">SYNTAX</span></span>

```
New-AzStorageAccountSASToken -Service <SharedAccessAccountServices>
 -ResourceType <SharedAccessAccountResourceTypes> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b7b3b-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="b7b3b-105">DESCRIPTION</span></span>
<span data-ttu-id="b7b3b-106">Polecenie cmdlet **New-AzStorageSASToken** tworzy token SAS (Shared Access Signature) na poziomie konta dla konta usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="b7b3b-106">The **New-AzStorageSASToken** cmdlet creates an account-level shared access signature (SAS) token for an Azure Storage account.</span></span>
<span data-ttu-id="b7b3b-107">Tokenu SAS można użyć do delegowania uprawnień do wielu usług lub do delegowania uprawnień do usług, które nie są dostępne za pomocą tokenu SAS na poziomie obiektu.</span><span class="sxs-lookup"><span data-stu-id="b7b3b-107">You can use the SAS token to delegate permissions for multiple services, or to delegate permissions for services not available with an object-level SAS token.</span></span>

## <span data-ttu-id="b7b3b-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b7b3b-108">EXAMPLES</span></span>

### <span data-ttu-id="b7b3b-109">Przykład 1. Tworzenie tokenu SAS na poziomie konta z pełnymi uprawnieniami</span><span class="sxs-lookup"><span data-stu-id="b7b3b-109">Example 1: Create an account-level SAS token with full permission</span></span>
```
PS C:\> New-AzStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup"
```

<span data-ttu-id="b7b3b-110">To polecenie tworzy token SAS na poziomie konta z pełnymi uprawnieniami.</span><span class="sxs-lookup"><span data-stu-id="b7b3b-110">This command creates an account-level SAS token with full permission.</span></span>

### <span data-ttu-id="b7b3b-111">Przykład 2. Tworzenie tokenu SAS na poziomie konta dla zakresu adresów IP</span><span class="sxs-lookup"><span data-stu-id="b7b3b-111">Example 2: Create an account-level SAS token for a range of IP addresses</span></span>
```
PS C:\> New-AzStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup" -Protocol HttpsOnly -IPAddressOrRange 168.1.5.60-168.1.5.70
```

<span data-ttu-id="b7b3b-112">To polecenie tworzy token SAS na poziomie konta dla żądań HTTPS tylko z określonego zakresu adresów IP.</span><span class="sxs-lookup"><span data-stu-id="b7b3b-112">This command creates an account-level SAS token for HTTPS-only requests from the specified range of IP addresses.</span></span>

## <span data-ttu-id="b7b3b-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b7b3b-113">PARAMETERS</span></span>

### <span data-ttu-id="b7b3b-114">— kontekst</span><span class="sxs-lookup"><span data-stu-id="b7b3b-114">-Context</span></span>
<span data-ttu-id="b7b3b-115">Określa kontekst magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b7b3b-115">Specifies the Azure storage context.</span></span>
<span data-ttu-id="b7b3b-116">Aby uzyskać obiekt **AzureStorageContext,** możesz użyć New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b7b3b-116">You can use the New-AzStorageContext cmdlet to get an **AzureStorageContext** object.</span></span>

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

### <span data-ttu-id="b7b3b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7b3b-117">-DefaultProfile</span></span>
<span data-ttu-id="b7b3b-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b7b3b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7b3b-119">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="b7b3b-119">-ExpiryTime</span></span>
<span data-ttu-id="b7b3b-120">Określa czas, w którym podpis dostępu udostępnionego staje się nieprawidłowy.</span><span class="sxs-lookup"><span data-stu-id="b7b3b-120">Specifies the time at which the shared access signature becomes invalid.</span></span>

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

### <span data-ttu-id="b7b3b-121">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="b7b3b-121">-IPAddressOrRange</span></span>
<span data-ttu-id="b7b3b-122">Określa adres IP lub zakres adresów IP, z których mają być akceptowane żądania, na przykład 168.1.5.65 lub 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="b7b3b-122">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="b7b3b-123">Zakres jest włącznie.</span><span class="sxs-lookup"><span data-stu-id="b7b3b-123">The range is inclusive.</span></span>

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

### <span data-ttu-id="b7b3b-124">— Uprawnienie</span><span class="sxs-lookup"><span data-stu-id="b7b3b-124">-Permission</span></span>
<span data-ttu-id="b7b3b-125">Określa uprawnienia dla konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="b7b3b-125">Specifies the permissions for Storage account.</span></span>
<span data-ttu-id="b7b3b-126">Uprawnienia są prawidłowe tylko wtedy, gdy są zgodne z określonym typem zasobu.</span><span class="sxs-lookup"><span data-stu-id="b7b3b-126">Permissions are valid only if they match the specified resource type.</span></span>
<span data-ttu-id="b7b3b-127">Należy pamiętać, że jest to ciąg, taki jak `rwd` (w przypadku odczytu, zapisu i usunięcia).</span><span class="sxs-lookup"><span data-stu-id="b7b3b-127">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>
<span data-ttu-id="b7b3b-128">Aby uzyskać więcej informacji na temat akceptowalnych wartości uprawnień, zobacz Tworzenie sygnatury SAS konta http://go.microsoft.com/fwlink/?LinkId=799514</span><span class="sxs-lookup"><span data-stu-id="b7b3b-128">For more information about acceptable permission values, see Constructing an Account SAS http://go.microsoft.com/fwlink/?LinkId=799514</span></span>

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

### <span data-ttu-id="b7b3b-129">— Protokół</span><span class="sxs-lookup"><span data-stu-id="b7b3b-129">-Protocol</span></span>
<span data-ttu-id="b7b3b-130">Określa dozwolony protokół dla żądania dokonanego za pomocą sygnatury SAS konta.</span><span class="sxs-lookup"><span data-stu-id="b7b3b-130">Specifies the protocol permitted for a request made with the account SAS.</span></span>
<span data-ttu-id="b7b3b-131">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="b7b3b-131">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b7b3b-132">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="b7b3b-132">HttpsOnly</span></span>
- <span data-ttu-id="b7b3b-133">HttpsOrHttp Wartość domyślna to httpsorhttp.</span><span class="sxs-lookup"><span data-stu-id="b7b3b-133">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="b7b3b-134">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="b7b3b-134">-ResourceType</span></span>
<span data-ttu-id="b7b3b-135">Określa typy zasobów dostępne w tokenie SAS.</span><span class="sxs-lookup"><span data-stu-id="b7b3b-135">Specifies the resource types that are available with the SAS token.</span></span>
<span data-ttu-id="b7b3b-136">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="b7b3b-136">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b7b3b-137">Brak</span><span class="sxs-lookup"><span data-stu-id="b7b3b-137">None</span></span>
- <span data-ttu-id="b7b3b-138">Usługa</span><span class="sxs-lookup"><span data-stu-id="b7b3b-138">Service</span></span>
- <span data-ttu-id="b7b3b-139">Kontener</span><span class="sxs-lookup"><span data-stu-id="b7b3b-139">Container</span></span>
- <span data-ttu-id="b7b3b-140">Obiekt</span><span class="sxs-lookup"><span data-stu-id="b7b3b-140">Object</span></span>

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

### <span data-ttu-id="b7b3b-141">— Usługa</span><span class="sxs-lookup"><span data-stu-id="b7b3b-141">-Service</span></span>
<span data-ttu-id="b7b3b-142">Określa usługę.</span><span class="sxs-lookup"><span data-stu-id="b7b3b-142">Specifies the service.</span></span>
<span data-ttu-id="b7b3b-143">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="b7b3b-143">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b7b3b-144">Brak</span><span class="sxs-lookup"><span data-stu-id="b7b3b-144">None</span></span>
- <span data-ttu-id="b7b3b-145">Obiekt blob</span><span class="sxs-lookup"><span data-stu-id="b7b3b-145">Blob</span></span>
- <span data-ttu-id="b7b3b-146">Plik</span><span class="sxs-lookup"><span data-stu-id="b7b3b-146">File</span></span>
- <span data-ttu-id="b7b3b-147">Kolejka</span><span class="sxs-lookup"><span data-stu-id="b7b3b-147">Queue</span></span>
- <span data-ttu-id="b7b3b-148">Tabela</span><span class="sxs-lookup"><span data-stu-id="b7b3b-148">Table</span></span>

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

### <span data-ttu-id="b7b3b-149">— StartTime</span><span class="sxs-lookup"><span data-stu-id="b7b3b-149">-StartTime</span></span>
<span data-ttu-id="b7b3b-150">Określa czas (jako obiekt **DateTime),** w którym sygnatura SAS jest prawidłowa.</span><span class="sxs-lookup"><span data-stu-id="b7b3b-150">Specifies the time, as a **DateTime** object, at which the SAS becomes valid.</span></span>
<span data-ttu-id="b7b3b-151">Aby uzyskać obiekt **DateTime,** użyj Get-Date cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b7b3b-151">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="b7b3b-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7b3b-152">CommonParameters</span></span>
<span data-ttu-id="b7b3b-153">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7b3b-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7b3b-154">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7b3b-154">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7b3b-155">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b7b3b-155">INPUTS</span></span>

### <span data-ttu-id="b7b3b-156">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="b7b3b-156">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="b7b3b-157">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b7b3b-157">OUTPUTS</span></span>

### <span data-ttu-id="b7b3b-158">System.String</span><span class="sxs-lookup"><span data-stu-id="b7b3b-158">System.String</span></span>

## <span data-ttu-id="b7b3b-159">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b7b3b-159">NOTES</span></span>

## <span data-ttu-id="b7b3b-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b7b3b-160">RELATED LINKS</span></span>

[<span data-ttu-id="b7b3b-161">New-AzstorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="b7b3b-161">New-AzStorageBlobSASToken</span></span>](./New-AzStorageBlobSASToken.md)

[<span data-ttu-id="b7b3b-162">New-AzstorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="b7b3b-162">New-AzStorageContainerSASToken</span></span>](./New-AzStorageContainerSASToken.md)

[<span data-ttu-id="b7b3b-163">New-azstorageFilesasToken</span><span class="sxs-lookup"><span data-stu-id="b7b3b-163">New-AzStorageFileSASToken</span></span>](./New-AzStorageFileSASToken.md)

[<span data-ttu-id="b7b3b-164">New-AzStorageQueueSASToken</span><span class="sxs-lookup"><span data-stu-id="b7b3b-164">New-AzStorageQueueSASToken</span></span>](./New-AzStorageQueueSASToken.md)

[<span data-ttu-id="b7b3b-165">New-AzstorageShareSASToken</span><span class="sxs-lookup"><span data-stu-id="b7b3b-165">New-AzStorageShareSASToken</span></span>](./New-AzStorageShareSASToken.md)

[<span data-ttu-id="b7b3b-166">New-azstorageTableSASToken</span><span class="sxs-lookup"><span data-stu-id="b7b3b-166">New-AzStorageTableSASToken</span></span>](./New-AzStorageTableSASToken.md)


