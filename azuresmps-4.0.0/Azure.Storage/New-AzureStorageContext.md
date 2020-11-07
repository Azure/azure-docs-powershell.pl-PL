---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 383402B2-6B7C-41AB-AFF9-36C86156B0A9
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4db0b752e8bf887e899a4de6a8e4175eaa2d9855
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523677"
---
# <span data-ttu-id="7eb54-101">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="7eb54-101">New-AzureStorageContext</span></span>

## <span data-ttu-id="7eb54-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7eb54-102">SYNOPSIS</span></span>
<span data-ttu-id="7eb54-103">Tworzy kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="7eb54-103">Creates an Azure Storage context.</span></span>

## <span data-ttu-id="7eb54-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7eb54-104">SYNTAX</span></span>

### <span data-ttu-id="7eb54-105">AccountNameAndKey (domyślny)</span><span class="sxs-lookup"><span data-stu-id="7eb54-105">AccountNameAndKey (Default)</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="7eb54-106">AccountNameAndKeyEnvironment</span><span class="sxs-lookup"><span data-stu-id="7eb54-106">AccountNameAndKeyEnvironment</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 -Environment <String> [<CommonParameters>]
```

### <span data-ttu-id="7eb54-107">AnonymousAccount</span><span class="sxs-lookup"><span data-stu-id="7eb54-107">AnonymousAccount</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] [-Endpoint <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="7eb54-108">AnonymousAccountEnvironment</span><span class="sxs-lookup"><span data-stu-id="7eb54-108">AnonymousAccountEnvironment</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] -Environment <String>
 [<CommonParameters>]
```

### <span data-ttu-id="7eb54-109">SasToken</span><span class="sxs-lookup"><span data-stu-id="7eb54-109">SasToken</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> -SasToken <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="7eb54-110">SasTokenWithAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="7eb54-110">SasTokenWithAzureEnvironment</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> -SasToken <String> -Environment <String>
 [<CommonParameters>]
```

### <span data-ttu-id="7eb54-111">Elemencie</span><span class="sxs-lookup"><span data-stu-id="7eb54-111">ConnectionString</span></span>
```
New-AzureStorageContext -ConnectionString <String> [<CommonParameters>]
```

### <span data-ttu-id="7eb54-112">LocalDevelopment</span><span class="sxs-lookup"><span data-stu-id="7eb54-112">LocalDevelopment</span></span>
```
New-AzureStorageContext [-Local] [<CommonParameters>]
```

## <span data-ttu-id="7eb54-113">Opis</span><span class="sxs-lookup"><span data-stu-id="7eb54-113">DESCRIPTION</span></span>
<span data-ttu-id="7eb54-114">Polecenie cmdlet **New-AzureStorageContext** umożliwia utworzenie kontekstu usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="7eb54-114">The **New-AzureStorageContext** cmdlet creates an Azure Storage context.</span></span>

## <span data-ttu-id="7eb54-115">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7eb54-115">EXAMPLES</span></span>

### <span data-ttu-id="7eb54-116">Przykład 1. Tworzenie kontekstu przez określenie nazwy i klucza konta magazynu</span><span class="sxs-lookup"><span data-stu-id="7eb54-116">Example 1: Create a context by specifying a storage account name and key</span></span>
```
C:\PS>New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
```

<span data-ttu-id="7eb54-117">To polecenie tworzy kontekst dla konta o nazwie ContosoGeneral, który używa określonego klucza.</span><span class="sxs-lookup"><span data-stu-id="7eb54-117">This command creates a context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="7eb54-118">Przykład 2: Tworzenie kontekstu przez określenie parametrów połączenia</span><span class="sxs-lookup"><span data-stu-id="7eb54-118">Example 2: Create a context by specifying a connection string</span></span>
```
C:\PS>New-AzureStorageContext -ConnectionString "DefaultEndpointsProtocol=https;AccountName=ContosoGeneral;AccountKey=< Storage Key for ContosoGeneral ends with == >;"
```

<span data-ttu-id="7eb54-119">To polecenie tworzy kontekst na podstawie określonych parametrów połączenia dla konta ContosoGeneral.</span><span class="sxs-lookup"><span data-stu-id="7eb54-119">This command creates a context based on the specified connection string for the account ContosoGeneral.</span></span>

### <span data-ttu-id="7eb54-120">Przykład 3: Tworzenie kontekstu dla konta magazynu anonimowego</span><span class="sxs-lookup"><span data-stu-id="7eb54-120">Example 3: Create a context for an anonymous storage account</span></span>
```
C:\PS>New-AzureStorageContext -StorageAccountName "ContosoGeneral" -Anonymous -Protocol "http"
```

<span data-ttu-id="7eb54-121">To polecenie tworzy kontekst do anonimowego korzystania z konta o nazwie ContosoGeneral.</span><span class="sxs-lookup"><span data-stu-id="7eb54-121">This command creates a context for anonymous use for the account named ContosoGeneral.</span></span>
<span data-ttu-id="7eb54-122">To polecenie określa HTTP jako protokół połączenia.</span><span class="sxs-lookup"><span data-stu-id="7eb54-122">The command specifies HTTP as a connection protocol.</span></span>

### <span data-ttu-id="7eb54-123">Przykład 4: Tworzenie kontekstu za pomocą lokalnego konta magazynu opracowywania</span><span class="sxs-lookup"><span data-stu-id="7eb54-123">Example 4: Create a context by using the local development storage account</span></span>
```
C:\PS>New-AzureStorageContext -Local
```

<span data-ttu-id="7eb54-124">To polecenie tworzy kontekst za pomocą lokalnego konta magazynu dla deweloperów.</span><span class="sxs-lookup"><span data-stu-id="7eb54-124">This command creates a context by using the local development storage account.</span></span>
<span data-ttu-id="7eb54-125">Polecenie określa parametr *Local* .</span><span class="sxs-lookup"><span data-stu-id="7eb54-125">The command specifies the *Local* parameter.</span></span>

### <span data-ttu-id="7eb54-126">Przykład 5: uzyskiwanie kontenera dla lokalnego konta magazynu dewelopera</span><span class="sxs-lookup"><span data-stu-id="7eb54-126">Example 5: Get the container for the local developer storage account</span></span>
```
C:\PS>New-AzureStorageContext -Local | Get-AzureStorageContainer
```

<span data-ttu-id="7eb54-127">To polecenie tworzy kontekst przy użyciu lokalnego konta magazynu dla programistów, a następnie przekazuje nowy kontekst do polecenia cmdlet **Get-AzureStorageContainer** przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="7eb54-127">This command creates a context by using the local development storage account, and then passes the new context to the **Get-AzureStorageContainer** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="7eb54-128">Polecenie pobiera kontener magazynu platformy Azure dla konta magazynu lokalnego dla deweloperów.</span><span class="sxs-lookup"><span data-stu-id="7eb54-128">The command gets the Azure Storage container for the local developer storage account.</span></span>

### <span data-ttu-id="7eb54-129">Przykład 6: uzyskiwanie wielu kontenerów</span><span class="sxs-lookup"><span data-stu-id="7eb54-129">Example 6: Get multiple containers</span></span>
```
C:\PS>$Context01 = New-AzureStorageContext -Local 
PS C:\> $Context02 = New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
PS C:\> ($Context01, $Context02) | Get-AzureStorageContainer
```

<span data-ttu-id="7eb54-130">Pierwsze polecenie tworzy kontekst przy użyciu lokalnego konta magazynu dla programistów, a następnie przechowuje ten kontekst w zmiennej $Context 01.</span><span class="sxs-lookup"><span data-stu-id="7eb54-130">The first command creates a context by using the local development storage account, and then stores that context in the $Context01 variable.</span></span>

<span data-ttu-id="7eb54-131">Drugie polecenie tworzy kontekst dla konta o nazwie ContosoGeneral, który używa określonego klucza, a następnie zapisuje ten kontekst w zmiennej $Context 02.</span><span class="sxs-lookup"><span data-stu-id="7eb54-131">The second command creates a context for the account named ContosoGeneral that uses the specified key, and then stores that context in the $Context02 variable.</span></span>

<span data-ttu-id="7eb54-132">Polecenie ostatnie uzyskuje kontenery dla kontekstów przechowywanych w $Context 01 i $Context 02 przy użyciu polecenia **Get-AzureStorageContainer**.</span><span class="sxs-lookup"><span data-stu-id="7eb54-132">The final command gets the containers for the contexts stored in $Context01 and $Context02 by using **Get-AzureStorageContainer**.</span></span>

### <span data-ttu-id="7eb54-133">Przykład 7: Tworzenie kontekstu za pomocą punktu końcowego</span><span class="sxs-lookup"><span data-stu-id="7eb54-133">Example 7: Create a context with an endpoint</span></span>
```
C:\PS>New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Endpoint "contosoaccount.core.windows.net"
```

<span data-ttu-id="7eb54-134">To polecenie tworzy kontekst usługi Azure Storage o określonym punkcie końcowym magazynu.</span><span class="sxs-lookup"><span data-stu-id="7eb54-134">This command creates an Azure Storage context that has the specified storage endpoint.</span></span>
<span data-ttu-id="7eb54-135">Polecenie utworzy kontekst dla konta o nazwie ContosoGeneral, który używa określonego klucza.</span><span class="sxs-lookup"><span data-stu-id="7eb54-135">The command creates the context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="7eb54-136">Przykład 8: Tworzenie kontekstu za pomocą określonego środowiska</span><span class="sxs-lookup"><span data-stu-id="7eb54-136">Example 8: Create a context with a specified environment</span></span>
```
C:\PS>New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Environment "AzureChinaCloud"
```

<span data-ttu-id="7eb54-137">To polecenie tworzy kontekst usługi Azure Storage z określonym środowiskiem platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="7eb54-137">This command creates an Azure storage context that has the specified Azure environment.</span></span>
<span data-ttu-id="7eb54-138">Polecenie utworzy kontekst dla konta o nazwie ContosoGeneral, który używa określonego klucza.</span><span class="sxs-lookup"><span data-stu-id="7eb54-138">The command creates the context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="7eb54-139">Przykład 9: Tworzenie kontekstu za pomocą tokenu SAS</span><span class="sxs-lookup"><span data-stu-id="7eb54-139">Example 9: Create a context by using an SAS token</span></span>
```
C:\PS>$SasToken = New-AzureStorageContainerSASToken -Name "ContosoMain" -Permission "raud"
PS C:\> $Context = New-AzureStorageContext -StorageAccountName "ContosoGeneral" -SasToken $SasToken
PS C:\> $Context | Get-AzureStorageBlob -Container "ContosoMain"
```

<span data-ttu-id="7eb54-140">Pierwsze polecenie generuje token SAS przy użyciu polecenia cmdlet **New-AzureStorageContainerSASToken** dla kontenera o nazwie ContosoMain, a następnie zapisuje ten token w zmiennej $SasToken.</span><span class="sxs-lookup"><span data-stu-id="7eb54-140">The first command generates an SAS token by using the **New-AzureStorageContainerSASToken** cmdlet for the container named ContosoMain, and then stores that token in the $SasToken variable.</span></span>
<span data-ttu-id="7eb54-141">Token ten jest przeznaczony dla uprawnień Odczyt, Dodawanie, aktualizowanie i usuwanie.</span><span class="sxs-lookup"><span data-stu-id="7eb54-141">That token is for read, add, update, and delete permissions.</span></span>

<span data-ttu-id="7eb54-142">Drugie polecenie tworzy kontekst dla konta o nazwie ContosoGeneral, w którym jest używany token SAS przechowywany w $SasToken, a następnie przechowuje ten kontekst w zmiennej $Context.</span><span class="sxs-lookup"><span data-stu-id="7eb54-142">The second command creates a context for the account named ContosoGeneral that uses the SAS token stored in $SasToken, and then stores that context in the $Context variable.</span></span>

<span data-ttu-id="7eb54-143">W ostatnim poleceniu są wyświetlane wszystkie obiekty blob skojarzone z kontenerem o nazwie ContosoMain przy użyciu kontekstu przechowywanego w $Context.</span><span class="sxs-lookup"><span data-stu-id="7eb54-143">The final command lists all the blobs associated with the container named ContosoMain by using the context stored in $Context.</span></span>

## <span data-ttu-id="7eb54-144">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7eb54-144">PARAMETERS</span></span>

### <span data-ttu-id="7eb54-145">-Anonymous</span><span class="sxs-lookup"><span data-stu-id="7eb54-145">-Anonymous</span></span>
<span data-ttu-id="7eb54-146">Wskazuje, że to polecenie cmdlet tworzy kontekst usługi Azure Storage do logowania anonimowego.</span><span class="sxs-lookup"><span data-stu-id="7eb54-146">Indicates that this cmdlet creates an Azure Storage context for anonymous logon.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AnonymousAccount, AnonymousAccountEnvironment
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7eb54-147">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="7eb54-147">-ConnectionString</span></span>
<span data-ttu-id="7eb54-148">Określa parametry połączenia dla kontekstu usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="7eb54-148">Specifies a connection string for the Azure Storage context.</span></span>

```yaml
Type: String
Parameter Sets: ConnectionString
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7eb54-149">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="7eb54-149">-Endpoint</span></span>
<span data-ttu-id="7eb54-150">Określa punkt końcowy kontekstu usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="7eb54-150">Specifies the endpoint for the Azure Storage context.</span></span>

```yaml
Type: String
Parameter Sets: AccountNameAndKey, AnonymousAccount, SasToken
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7eb54-151">-Środowisko</span><span class="sxs-lookup"><span data-stu-id="7eb54-151">-Environment</span></span>
<span data-ttu-id="7eb54-152">Określa środowisko Azure.</span><span class="sxs-lookup"><span data-stu-id="7eb54-152">Specifies the Azure environment.</span></span>
<span data-ttu-id="7eb54-153">Dopuszczalne wartości tego parametru to: AzureCloud oraz AzureChinaCloud.</span><span class="sxs-lookup"><span data-stu-id="7eb54-153">The acceptable values for this parameter are: AzureCloud and AzureChinaCloud.</span></span>
<span data-ttu-id="7eb54-154">Aby uzyskać więcej informacji, wpisz tekst `Get-Help Get-AzureEnvironment` .</span><span class="sxs-lookup"><span data-stu-id="7eb54-154">For more information, type `Get-Help Get-AzureEnvironment`.</span></span>

```yaml
Type: String
Parameter Sets: AccountNameAndKeyEnvironment, AnonymousAccountEnvironment
Aliases: Name, EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SasTokenWithAzureEnvironment
Aliases: Name, EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7eb54-155">-Local</span><span class="sxs-lookup"><span data-stu-id="7eb54-155">-Local</span></span>
<span data-ttu-id="7eb54-156">Wskazuje, że to polecenie cmdlet tworzy kontekst przy użyciu lokalnego konta magazynu dla deweloperów.</span><span class="sxs-lookup"><span data-stu-id="7eb54-156">Indicates that this cmdlet creates a context by using the local development storage account.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: LocalDevelopment
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7eb54-157">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="7eb54-157">-Protocol</span></span>
<span data-ttu-id="7eb54-158">Umożliwia określenie protokołu dozwolonego dla żądania wykonywanego za pomocą skojarzeń zabezpieczeń konta.</span><span class="sxs-lookup"><span data-stu-id="7eb54-158">Specifies the protocol permitted for a request made with the account SAS.</span></span>
<span data-ttu-id="7eb54-159">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="7eb54-159">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7eb54-160">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="7eb54-160">HttpsOnly</span></span>
- <span data-ttu-id="7eb54-161">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="7eb54-161">HttpsOrHttp</span></span>

<span data-ttu-id="7eb54-162">Wartość domyślna to HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="7eb54-162">The default value is HttpsOrHttp.</span></span>

```yaml
Type: String
Parameter Sets: AccountNameAndKey, AccountNameAndKeyEnvironment, AnonymousAccount, AnonymousAccountEnvironment, SasToken
Aliases: 
Accepted values: Http, Https

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7eb54-163">-SasToken</span><span class="sxs-lookup"><span data-stu-id="7eb54-163">-SasToken</span></span>
<span data-ttu-id="7eb54-164">Określa token funkcji dostępu współużytkowanego (SAS, Access Signature) dla kontekstu.</span><span class="sxs-lookup"><span data-stu-id="7eb54-164">Specifies a Shared Access Signature (SAS) token for the context.</span></span>

```yaml
Type: String
Parameter Sets: SasToken, SasTokenWithAzureEnvironment
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7eb54-165">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="7eb54-165">-StorageAccountKey</span></span>
<span data-ttu-id="7eb54-166">Określa klucz konta usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="7eb54-166">Specifies an Azure Storage account key.</span></span>
<span data-ttu-id="7eb54-167">To polecenie cmdlet tworzy kontekst dla klucza, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="7eb54-167">This cmdlet creates a context for the key that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: AccountNameAndKey, AccountNameAndKeyEnvironment
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7eb54-168">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="7eb54-168">-StorageAccountName</span></span>
<span data-ttu-id="7eb54-169">Określa nazwę konta magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="7eb54-169">Specifies an Azure Storage account name.</span></span>
<span data-ttu-id="7eb54-170">To polecenie cmdlet tworzy kontekst dla konta, które określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="7eb54-170">This cmdlet creates a context for the account that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: AccountNameAndKey, AccountNameAndKeyEnvironment, AnonymousAccount, AnonymousAccountEnvironment, SasToken, SasTokenWithAzureEnvironment
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7eb54-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7eb54-171">CommonParameters</span></span>
<span data-ttu-id="7eb54-172">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7eb54-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7eb54-173">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7eb54-173">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7eb54-174">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7eb54-174">INPUTS</span></span>

## <span data-ttu-id="7eb54-175">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7eb54-175">OUTPUTS</span></span>

### <span data-ttu-id="7eb54-176">AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="7eb54-176">AzureStorageContext</span></span>

## <span data-ttu-id="7eb54-177">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7eb54-177">NOTES</span></span>

## <span data-ttu-id="7eb54-178">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7eb54-178">RELATED LINKS</span></span>

[<span data-ttu-id="7eb54-179">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="7eb54-179">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="7eb54-180">Nowe — AzureStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="7eb54-180">New-AzureStorageContainerSASToken</span></span>](./New-AzureStorageContainerSASToken.md)

