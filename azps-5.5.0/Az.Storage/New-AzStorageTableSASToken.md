---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 3CFA6E31-E243-4B22-AE8F-1942DD324639
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragetablesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTableSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTableSASToken.md
ms.openlocfilehash: bf17a44b4f67d545ed464670776a5fc4c81b315a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190834"
---
# <span data-ttu-id="5a0a6-101">New-AzStorageTableSASToken</span><span class="sxs-lookup"><span data-stu-id="5a0a6-101">New-AzStorageTableSASToken</span></span>

## <span data-ttu-id="5a0a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a0a6-102">SYNOPSIS</span></span>
<span data-ttu-id="5a0a6-103">Generuje token SAS dla tabeli magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5a0a6-103">Generates an SAS token for an Azure Storage table.</span></span>

## <span data-ttu-id="5a0a6-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5a0a6-104">SYNTAX</span></span>

### <span data-ttu-id="5a0a6-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="5a0a6-105">SasPolicy</span></span>
```
New-AzStorageTableSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-StartPartitionKey <String>] [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5a0a6-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="5a0a6-106">SasPermission</span></span>
```
New-AzStorageTableSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-StartPartitionKey <String>] [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5a0a6-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="5a0a6-107">DESCRIPTION</span></span>
<span data-ttu-id="5a0a6-108">Polecenie cmdlet **New-AzStorageTableSASToken** generuje token SAS (Shared Access Signature) dla tabeli magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5a0a6-108">The **New-AzStorageTableSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure Storage table.</span></span>

## <span data-ttu-id="5a0a6-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5a0a6-109">EXAMPLES</span></span>

### <span data-ttu-id="5a0a6-110">Przykład 1. Generowanie tokenu SAS z pełnymi uprawnieniami do tabeli</span><span class="sxs-lookup"><span data-stu-id="5a0a6-110">Example 1: Generate an SAS token that has full permissions for a table</span></span>
```
C:\PS>New-AzStorageTableSASToken -Name "ContosoResources" -Permission "raud"
```

<span data-ttu-id="5a0a6-111">To polecenie generuje token SAS z pełnymi uprawnieniami do tabeli o nazwie ContosoResources.</span><span class="sxs-lookup"><span data-stu-id="5a0a6-111">This command generates an SAS token with full permissions for the table named ContosoResources.</span></span>
<span data-ttu-id="5a0a6-112">Token ten jest do odczytu, dodawania, aktualizowania i usuwania uprawnień.</span><span class="sxs-lookup"><span data-stu-id="5a0a6-112">That token is for read, add, update, and delete permissions.</span></span>

### <span data-ttu-id="5a0a6-113">Przykład 2. Generowanie tokenu SAS dla zakresu partycji</span><span class="sxs-lookup"><span data-stu-id="5a0a6-113">Example 2: Generate an SAS token for a range of partitions</span></span>
```
C:\PS>New-AzStorageTableSASToken -Name "ContosoResources" -Permission "raud" -StartPartitionKey "a" -EndPartitionKey "b"
```

<span data-ttu-id="5a0a6-114">To polecenie generuje i token SAS z pełnymi uprawnieniami do tabeli o nazwie ContosoResources.</span><span class="sxs-lookup"><span data-stu-id="5a0a6-114">This command generates and SAS token with full permissions for the table named ContosoResources.</span></span>
<span data-ttu-id="5a0a6-115">To polecenie ogranicza token do zakresu, który określają parametry *KluczSkładnikaSkładu* i KluczSkładnikaNaskładu Końcowego. </span><span class="sxs-lookup"><span data-stu-id="5a0a6-115">The command limits the token to the range that the *StartPartitionKey* and *EndPartitionKey* parameters specify.</span></span>

### <span data-ttu-id="5a0a6-116">Przykład 3. Generowanie tokenu SAS, który ma przechowywane zasady dostępu dla tabeli</span><span class="sxs-lookup"><span data-stu-id="5a0a6-116">Example 3: Generate an SAS token that has a stored access policy for a table</span></span>
```
C:\PS>New-AzStorageTableSASToken -Name "ContosoResources" -Policy "ClientPolicy01"
```

<span data-ttu-id="5a0a6-117">To polecenie generuje token SAS dla tabeli o nazwie ContosoResources.</span><span class="sxs-lookup"><span data-stu-id="5a0a6-117">This command generates an SAS token for the table named ContosoResources.</span></span>
<span data-ttu-id="5a0a6-118">To polecenie określa przechowywane zasady dostępu o nazwie ClientPolicy01.</span><span class="sxs-lookup"><span data-stu-id="5a0a6-118">The command specifies the stored access policy named ClientPolicy01.</span></span>

## <span data-ttu-id="5a0a6-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5a0a6-119">PARAMETERS</span></span>

### <span data-ttu-id="5a0a6-120">— kontekst</span><span class="sxs-lookup"><span data-stu-id="5a0a6-120">-Context</span></span>
<span data-ttu-id="5a0a6-121">Określa kontekst magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5a0a6-121">Specifies an Azure storage context.</span></span>
<span data-ttu-id="5a0a6-122">Aby uzyskać kontekst magazynowania, użyj New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a0a6-122">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="5a0a6-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a0a6-123">-DefaultProfile</span></span>
<span data-ttu-id="5a0a6-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="5a0a6-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a0a6-125">-EndPartitionKey</span><span class="sxs-lookup"><span data-stu-id="5a0a6-125">-EndPartitionKey</span></span>
<span data-ttu-id="5a0a6-126">Określa klucz partycji na końcu zakresu dla tokenu, który tworzy to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a0a6-126">Specifies the partition key of the end of the range for the token that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: endpk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a0a6-127">-EndRowKey</span><span class="sxs-lookup"><span data-stu-id="5a0a6-127">-EndRowKey</span></span>
<span data-ttu-id="5a0a6-128">Określa klucz wiersza dla końca zakresu dla tokenu, który tworzy to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a0a6-128">Specifies the row key for the end of the range for the token that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: endrk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a0a6-129">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="5a0a6-129">-ExpiryTime</span></span>
<span data-ttu-id="5a0a6-130">Określa, kiedy wygasa token SAS.</span><span class="sxs-lookup"><span data-stu-id="5a0a6-130">Specifies when the SAS token expires.</span></span>

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

### <span data-ttu-id="5a0a6-131">-FullUri</span><span class="sxs-lookup"><span data-stu-id="5a0a6-131">-FullUri</span></span>
<span data-ttu-id="5a0a6-132">Wskazuje, że to polecenie cmdlet zwraca pełny URI kolejki z tokenem SAS.</span><span class="sxs-lookup"><span data-stu-id="5a0a6-132">Indicates that this cmdlet returns the full queue URI with the SAS token.</span></span>

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

### <span data-ttu-id="5a0a6-133">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="5a0a6-133">-IPAddressOrRange</span></span>
<span data-ttu-id="5a0a6-134">Określa adres IP lub zakres adresów IP, z których mają być akceptowane żądania, na przykład 168.1.5.65 lub 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="5a0a6-134">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="5a0a6-135">Zakres jest włącznie.</span><span class="sxs-lookup"><span data-stu-id="5a0a6-135">The range is inclusive.</span></span>

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

### <span data-ttu-id="5a0a6-136">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="5a0a6-136">-Name</span></span>
<span data-ttu-id="5a0a6-137">Określa nazwę tabeli magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5a0a6-137">Specifies the name of an Azure Storage table.</span></span>
<span data-ttu-id="5a0a6-138">To polecenie cmdlet tworzy token SAS dla tabeli, która określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="5a0a6-138">This cmdlet creates an SAS token for the table that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Table

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5a0a6-139">— Uprawnienie</span><span class="sxs-lookup"><span data-stu-id="5a0a6-139">-Permission</span></span>
<span data-ttu-id="5a0a6-140">Określa uprawnienia dla tabeli magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5a0a6-140">Specifies permissions for an Azure Storage table.</span></span>
<span data-ttu-id="5a0a6-141">Należy pamiętać, że jest to ciąg, taki jak `rwd` (w przypadku odczytu, zapisu i usunięcia).</span><span class="sxs-lookup"><span data-stu-id="5a0a6-141">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="5a0a6-142">— Zasady</span><span class="sxs-lookup"><span data-stu-id="5a0a6-142">-Policy</span></span>
<span data-ttu-id="5a0a6-143">Określa zasady przechowywanego dostępu, które zawierają uprawnienia dla tego tokenu SAS.</span><span class="sxs-lookup"><span data-stu-id="5a0a6-143">Specifies a stored access policy, which includes the permissions for this SAS token.</span></span>

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

### <span data-ttu-id="5a0a6-144">— Protokół</span><span class="sxs-lookup"><span data-stu-id="5a0a6-144">-Protocol</span></span>
<span data-ttu-id="5a0a6-145">Określa protokół dozwolony dla żądania.</span><span class="sxs-lookup"><span data-stu-id="5a0a6-145">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="5a0a6-146">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="5a0a6-146">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="5a0a6-147">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="5a0a6-147">HttpsOnly</span></span>
* <span data-ttu-id="5a0a6-148">HttpsOrHttp Wartość domyślna to httpsorhttp.</span><span class="sxs-lookup"><span data-stu-id="5a0a6-148">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Cosmos.Table.SharedAccessProtocol]
Parameter Sets: (All)
Aliases:
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a0a6-149">-StartPartitionKey</span><span class="sxs-lookup"><span data-stu-id="5a0a6-149">-StartPartitionKey</span></span>
<span data-ttu-id="5a0a6-150">Określa klucz partycji dla początku zakresu dla tokenu, który tworzy to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a0a6-150">Specifies the partition key of the start of the range for the token that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: startpk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a0a6-151">-StartRowKey</span><span class="sxs-lookup"><span data-stu-id="5a0a6-151">-StartRowKey</span></span>
<span data-ttu-id="5a0a6-152">Określa klucz wiersza dla początku zakresu dla tokenu, który tworzy to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a0a6-152">Specifies the row key for the start of the range for the token that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: startrk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a0a6-153">— StartTime</span><span class="sxs-lookup"><span data-stu-id="5a0a6-153">-StartTime</span></span>
<span data-ttu-id="5a0a6-154">Określa, kiedy token SAS stanie się prawidłowy.</span><span class="sxs-lookup"><span data-stu-id="5a0a6-154">Specifies when the SAS token becomes valid.</span></span>

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

### <span data-ttu-id="5a0a6-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a0a6-155">CommonParameters</span></span>
<span data-ttu-id="5a0a6-156">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a0a6-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a0a6-157">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a0a6-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a0a6-158">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5a0a6-158">INPUTS</span></span>

### <span data-ttu-id="5a0a6-159">System.String</span><span class="sxs-lookup"><span data-stu-id="5a0a6-159">System.String</span></span>

### <span data-ttu-id="5a0a6-160">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="5a0a6-160">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="5a0a6-161">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5a0a6-161">OUTPUTS</span></span>

### <span data-ttu-id="5a0a6-162">System.String</span><span class="sxs-lookup"><span data-stu-id="5a0a6-162">System.String</span></span>

## <span data-ttu-id="5a0a6-163">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5a0a6-163">NOTES</span></span>

## <span data-ttu-id="5a0a6-164">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5a0a6-164">RELATED LINKS</span></span>

[<span data-ttu-id="5a0a6-165">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="5a0a6-165">New-AzStorageContext</span></span>](./New-AzStorageContext.md)
