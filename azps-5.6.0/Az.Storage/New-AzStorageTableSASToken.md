---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 3CFA6E31-E243-4B22-AE8F-1942DD324639
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstoragetablesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTableSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTableSASToken.md
ms.openlocfilehash: 65a90f703f142a01429fb215bd5c66bef74bb4c8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008298"
---
# <span data-ttu-id="de62b-101">New-AzStorageTableSASToken</span><span class="sxs-lookup"><span data-stu-id="de62b-101">New-AzStorageTableSASToken</span></span>

## <span data-ttu-id="de62b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="de62b-102">SYNOPSIS</span></span>
<span data-ttu-id="de62b-103">Generuje token SAS dla tabeli magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="de62b-103">Generates an SAS token for an Azure Storage table.</span></span>

## <span data-ttu-id="de62b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="de62b-104">SYNTAX</span></span>

### <span data-ttu-id="de62b-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="de62b-105">SasPolicy</span></span>
```
New-AzStorageTableSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-StartPartitionKey <String>] [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="de62b-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="de62b-106">SasPermission</span></span>
```
New-AzStorageTableSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-StartPartitionKey <String>] [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="de62b-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="de62b-107">DESCRIPTION</span></span>
<span data-ttu-id="de62b-108">Polecenie **cmdlet New-AzStorageTableSASToken** generuje token SAS (Shared Access Signature) dla tabeli magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="de62b-108">The **New-AzStorageTableSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure Storage table.</span></span>

## <span data-ttu-id="de62b-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="de62b-109">EXAMPLES</span></span>

### <span data-ttu-id="de62b-110">Przykład 1. Generowanie tokenu SAS z pełnymi uprawnieniami do tabeli</span><span class="sxs-lookup"><span data-stu-id="de62b-110">Example 1: Generate an SAS token that has full permissions for a table</span></span>
```
C:\PS>New-AzStorageTableSASToken -Name "ContosoResources" -Permission "raud"
```

<span data-ttu-id="de62b-111">To polecenie generuje token SAS z pełnymi uprawnieniami do tabeli o nazwie ContosoResources.</span><span class="sxs-lookup"><span data-stu-id="de62b-111">This command generates an SAS token with full permissions for the table named ContosoResources.</span></span>
<span data-ttu-id="de62b-112">Token ten jest do odczytu, dodawania, aktualizowania i usuwania uprawnień.</span><span class="sxs-lookup"><span data-stu-id="de62b-112">That token is for read, add, update, and delete permissions.</span></span>

### <span data-ttu-id="de62b-113">Przykład 2. Generowanie tokenu SAS dla zakresu partycji</span><span class="sxs-lookup"><span data-stu-id="de62b-113">Example 2: Generate an SAS token for a range of partitions</span></span>
```
C:\PS>New-AzStorageTableSASToken -Name "ContosoResources" -Permission "raud" -StartPartitionKey "a" -EndPartitionKey "b"
```

<span data-ttu-id="de62b-114">To polecenie generuje i token SAS z pełnymi uprawnieniami do tabeli o nazwie ContosoResources.</span><span class="sxs-lookup"><span data-stu-id="de62b-114">This command generates and SAS token with full permissions for the table named ContosoResources.</span></span>
<span data-ttu-id="de62b-115">To polecenie ogranicza token do zakresu, który określają parametry *KluczSkładnikaSkładu* i KluczSkładnikaNaskładu Końcowego. </span><span class="sxs-lookup"><span data-stu-id="de62b-115">The command limits the token to the range that the *StartPartitionKey* and *EndPartitionKey* parameters specify.</span></span>

### <span data-ttu-id="de62b-116">Przykład 3. Generowanie tokenu SAS, który ma przechowywane zasady dostępu dla tabeli</span><span class="sxs-lookup"><span data-stu-id="de62b-116">Example 3: Generate an SAS token that has a stored access policy for a table</span></span>
```
C:\PS>New-AzStorageTableSASToken -Name "ContosoResources" -Policy "ClientPolicy01"
```

<span data-ttu-id="de62b-117">To polecenie generuje token SAS dla tabeli o nazwie ContosoResources.</span><span class="sxs-lookup"><span data-stu-id="de62b-117">This command generates an SAS token for the table named ContosoResources.</span></span>
<span data-ttu-id="de62b-118">To polecenie określa przechowywane zasady dostępu o nazwie ClientPolicy01.</span><span class="sxs-lookup"><span data-stu-id="de62b-118">The command specifies the stored access policy named ClientPolicy01.</span></span>

## <span data-ttu-id="de62b-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="de62b-119">PARAMETERS</span></span>

### <span data-ttu-id="de62b-120">— kontekst</span><span class="sxs-lookup"><span data-stu-id="de62b-120">-Context</span></span>
<span data-ttu-id="de62b-121">Określa kontekst magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="de62b-121">Specifies an Azure storage context.</span></span>
<span data-ttu-id="de62b-122">Aby uzyskać kontekst magazynu, użyj New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="de62b-122">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="de62b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de62b-123">-DefaultProfile</span></span>
<span data-ttu-id="de62b-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="de62b-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de62b-125">-EndPartitionKey</span><span class="sxs-lookup"><span data-stu-id="de62b-125">-EndPartitionKey</span></span>
<span data-ttu-id="de62b-126">Określa klucz partycji na końcu zakresu dla tokenu, który tworzy to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="de62b-126">Specifies the partition key of the end of the range for the token that this cmdlet creates.</span></span>

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

### <span data-ttu-id="de62b-127">-EndRowKey</span><span class="sxs-lookup"><span data-stu-id="de62b-127">-EndRowKey</span></span>
<span data-ttu-id="de62b-128">Określa klucz wiersza dla końca zakresu dla tokenu, który tworzy to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="de62b-128">Specifies the row key for the end of the range for the token that this cmdlet creates.</span></span>

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

### <span data-ttu-id="de62b-129">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="de62b-129">-ExpiryTime</span></span>
<span data-ttu-id="de62b-130">Określa, kiedy wygasa token SAS.</span><span class="sxs-lookup"><span data-stu-id="de62b-130">Specifies when the SAS token expires.</span></span>

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

### <span data-ttu-id="de62b-131">-FullUri</span><span class="sxs-lookup"><span data-stu-id="de62b-131">-FullUri</span></span>
<span data-ttu-id="de62b-132">Wskazuje, że to polecenie cmdlet zwraca pełny URI kolejki z tokenem SAS.</span><span class="sxs-lookup"><span data-stu-id="de62b-132">Indicates that this cmdlet returns the full queue URI with the SAS token.</span></span>

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

### <span data-ttu-id="de62b-133">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="de62b-133">-IPAddressOrRange</span></span>
<span data-ttu-id="de62b-134">Określa adres IP lub zakres adresów IP, z których mają być akceptowane żądania, na przykład 168.1.5.65 lub 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="de62b-134">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="de62b-135">Zakres jest włącznie.</span><span class="sxs-lookup"><span data-stu-id="de62b-135">The range is inclusive.</span></span>

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

### <span data-ttu-id="de62b-136">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="de62b-136">-Name</span></span>
<span data-ttu-id="de62b-137">Określa nazwę tabeli magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="de62b-137">Specifies the name of an Azure Storage table.</span></span>
<span data-ttu-id="de62b-138">To polecenie cmdlet tworzy token SAS dla tabeli, która określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="de62b-138">This cmdlet creates an SAS token for the table that this parameter specifies.</span></span>

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

### <span data-ttu-id="de62b-139">— Uprawnienie</span><span class="sxs-lookup"><span data-stu-id="de62b-139">-Permission</span></span>
<span data-ttu-id="de62b-140">Określa uprawnienia dla tabeli magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="de62b-140">Specifies permissions for an Azure Storage table.</span></span>
<span data-ttu-id="de62b-141">Należy pamiętać, że jest to ciąg, taki jak `rwd` (w przypadku odczytu, zapisu i usunięcia).</span><span class="sxs-lookup"><span data-stu-id="de62b-141">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="de62b-142">— Zasady</span><span class="sxs-lookup"><span data-stu-id="de62b-142">-Policy</span></span>
<span data-ttu-id="de62b-143">Określa zasady przechowywanego dostępu, które zawierają uprawnienia dla tego tokenu SAS.</span><span class="sxs-lookup"><span data-stu-id="de62b-143">Specifies a stored access policy, which includes the permissions for this SAS token.</span></span>

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

### <span data-ttu-id="de62b-144">— Protokół</span><span class="sxs-lookup"><span data-stu-id="de62b-144">-Protocol</span></span>
<span data-ttu-id="de62b-145">Określa protokół dozwolony dla żądania.</span><span class="sxs-lookup"><span data-stu-id="de62b-145">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="de62b-146">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="de62b-146">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="de62b-147">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="de62b-147">HttpsOnly</span></span>
* <span data-ttu-id="de62b-148">HttpsOrHttp Wartość domyślna to httpsorhttp.</span><span class="sxs-lookup"><span data-stu-id="de62b-148">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="de62b-149">-StartPartitionKey</span><span class="sxs-lookup"><span data-stu-id="de62b-149">-StartPartitionKey</span></span>
<span data-ttu-id="de62b-150">Określa klucz partycji dla początku zakresu dla tokenu, który tworzy to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="de62b-150">Specifies the partition key of the start of the range for the token that this cmdlet creates.</span></span>

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

### <span data-ttu-id="de62b-151">-StartRowKey</span><span class="sxs-lookup"><span data-stu-id="de62b-151">-StartRowKey</span></span>
<span data-ttu-id="de62b-152">Określa klucz wiersza dla początku zakresu dla tokenu, który tworzy to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="de62b-152">Specifies the row key for the start of the range for the token that this cmdlet creates.</span></span>

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

### <span data-ttu-id="de62b-153">— StartTime</span><span class="sxs-lookup"><span data-stu-id="de62b-153">-StartTime</span></span>
<span data-ttu-id="de62b-154">Określa, kiedy token SAS stanie się prawidłowy.</span><span class="sxs-lookup"><span data-stu-id="de62b-154">Specifies when the SAS token becomes valid.</span></span>

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

### <span data-ttu-id="de62b-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de62b-155">CommonParameters</span></span>
<span data-ttu-id="de62b-156">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de62b-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de62b-157">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de62b-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de62b-158">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="de62b-158">INPUTS</span></span>

### <span data-ttu-id="de62b-159">System.String</span><span class="sxs-lookup"><span data-stu-id="de62b-159">System.String</span></span>

### <span data-ttu-id="de62b-160">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="de62b-160">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="de62b-161">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="de62b-161">OUTPUTS</span></span>

### <span data-ttu-id="de62b-162">System.String</span><span class="sxs-lookup"><span data-stu-id="de62b-162">System.String</span></span>

## <span data-ttu-id="de62b-163">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="de62b-163">NOTES</span></span>

## <span data-ttu-id="de62b-164">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="de62b-164">RELATED LINKS</span></span>

[<span data-ttu-id="de62b-165">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="de62b-165">New-AzStorageContext</span></span>](./New-AzStorageContext.md)
