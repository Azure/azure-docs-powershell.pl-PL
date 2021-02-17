---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 383402B2-6B7C-41AB-AFF9-36C86156B0A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragecontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContext.md
ms.openlocfilehash: ae12bb509773f36ecfd94ad6907499f0b5feb02d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100241866"
---
# <span data-ttu-id="feda0-101">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="feda0-101">New-AzStorageContext</span></span>

## <span data-ttu-id="feda0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="feda0-102">SYNOPSIS</span></span>
<span data-ttu-id="feda0-103">Tworzy kontekst magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="feda0-103">Creates an Azure Storage context.</span></span>

## <span data-ttu-id="feda0-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="feda0-104">SYNTAX</span></span>

### <span data-ttu-id="feda0-105">OAuthAccount (domyślne)</span><span class="sxs-lookup"><span data-stu-id="feda0-105">OAuthAccount (Default)</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-UseConnectedAccount] [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="feda0-106">AccountNameAndKey</span><span class="sxs-lookup"><span data-stu-id="feda0-106">AccountNameAndKey</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="feda0-107">AccountNameAndKeyEnvironment</span><span class="sxs-lookup"><span data-stu-id="feda0-107">AccountNameAndKeyEnvironment</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 -Environment <String> [<CommonParameters>]
```

### <span data-ttu-id="feda0-108">AnonymousAccount</span><span class="sxs-lookup"><span data-stu-id="feda0-108">AnonymousAccount</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] [-Endpoint <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="feda0-109">AnonymousAccountEnvironment</span><span class="sxs-lookup"><span data-stu-id="feda0-109">AnonymousAccountEnvironment</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] -Environment <String>
 [<CommonParameters>]
```

### <span data-ttu-id="feda0-110">SasToken</span><span class="sxs-lookup"><span data-stu-id="feda0-110">SasToken</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> -SasToken <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="feda0-111">SasTokenWithAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="feda0-111">SasTokenWithAzureEnvironment</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> -SasToken <String> -Environment <String>
 [<CommonParameters>]
```

### <span data-ttu-id="feda0-112">OAuthAccountEnvironment</span><span class="sxs-lookup"><span data-stu-id="feda0-112">OAuthAccountEnvironment</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-UseConnectedAccount] [-Protocol <String>]
 -Environment <String> [<CommonParameters>]
```

### <span data-ttu-id="feda0-113">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="feda0-113">ConnectionString</span></span>
```
New-AzStorageContext -ConnectionString <String> [<CommonParameters>]
```

### <span data-ttu-id="feda0-114">LocalDevelopment</span><span class="sxs-lookup"><span data-stu-id="feda0-114">LocalDevelopment</span></span>
```
New-AzStorageContext [-Local] [<CommonParameters>]
```

## <span data-ttu-id="feda0-115">OPIS</span><span class="sxs-lookup"><span data-stu-id="feda0-115">DESCRIPTION</span></span>
<span data-ttu-id="feda0-116">Polecenie **cmdlet New-AzStorageContext** tworzy kontekst magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="feda0-116">The **New-AzStorageContext** cmdlet creates an Azure Storage context.</span></span>
<span data-ttu-id="feda0-117">Domyślnym uwierzytelnianiem kontekstu magazynu jest OAuth (Azure AD), jeśli jest to nazwa konta magazynu wejściowego.</span><span class="sxs-lookup"><span data-stu-id="feda0-117">The default Authentication of a Storage Context is OAuth (Azure AD), if only input Storage account name.</span></span>
<span data-ttu-id="feda0-118">Zobacz szczegóły uwierzytelniania usługi magazynu https://docs.microsoft.com/en-us/rest/api/storageservices/authorization-for-the-azure-storage-services w.</span><span class="sxs-lookup"><span data-stu-id="feda0-118">See details of authentication of the Storage Service in https://docs.microsoft.com/en-us/rest/api/storageservices/authorization-for-the-azure-storage-services.</span></span>

## <span data-ttu-id="feda0-119">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="feda0-119">EXAMPLES</span></span>

### <span data-ttu-id="feda0-120">Przykład 1. Tworzenie kontekstu przez określenie nazwy i klucza konta magazynu</span><span class="sxs-lookup"><span data-stu-id="feda0-120">Example 1: Create a context by specifying a storage account name and key</span></span>
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
```

<span data-ttu-id="feda0-121">To polecenie tworzy kontekst dla konta o nazwie ContosoGeneral, które używa określonego klucza.</span><span class="sxs-lookup"><span data-stu-id="feda0-121">This command creates a context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="feda0-122">Przykład 2. Tworzenie kontekstu przez określenie parametrów połączenia</span><span class="sxs-lookup"><span data-stu-id="feda0-122">Example 2: Create a context by specifying a connection string</span></span>
```
PS C:\>New-AzStorageContext -ConnectionString "DefaultEndpointsProtocol=https;AccountName=ContosoGeneral;AccountKey=< Storage Key for ContosoGeneral ends with == >;"
```

<span data-ttu-id="feda0-123">To polecenie tworzy kontekst na podstawie określonych parametrów połączenia dla konta ContosoGeneral.</span><span class="sxs-lookup"><span data-stu-id="feda0-123">This command creates a context based on the specified connection string for the account ContosoGeneral.</span></span>

### <span data-ttu-id="feda0-124">Przykład 3. Tworzenie kontekstu dla anonimowego konta magazynu</span><span class="sxs-lookup"><span data-stu-id="feda0-124">Example 3: Create a context for an anonymous storage account</span></span>
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -Anonymous -Protocol "http"
```

<span data-ttu-id="feda0-125">To polecenie tworzy kontekst do użytku anonimowego dla konta o nazwie ContosoGeneral.</span><span class="sxs-lookup"><span data-stu-id="feda0-125">This command creates a context for anonymous use for the account named ContosoGeneral.</span></span>
<span data-ttu-id="feda0-126">To polecenie określa protokół HTTP jako protokół połączenia.</span><span class="sxs-lookup"><span data-stu-id="feda0-126">The command specifies HTTP as a connection protocol.</span></span>

### <span data-ttu-id="feda0-127">Przykład 4. Tworzenie kontekstu przy użyciu konta magazynu dla rozwoju lokalnego</span><span class="sxs-lookup"><span data-stu-id="feda0-127">Example 4: Create a context by using the local development storage account</span></span>
```
PS C:\>New-AzStorageContext -Local
```

<span data-ttu-id="feda0-128">To polecenie tworzy kontekst przy użyciu lokalnego konta magazynu programowego.</span><span class="sxs-lookup"><span data-stu-id="feda0-128">This command creates a context by using the local development storage account.</span></span>
<span data-ttu-id="feda0-129">Polecenie określa *parametr Local.*</span><span class="sxs-lookup"><span data-stu-id="feda0-129">The command specifies the *Local* parameter.</span></span>

### <span data-ttu-id="feda0-130">Przykład 5. Uzyskiwanie kontenera dla lokalnego konta magazynu dewelopera</span><span class="sxs-lookup"><span data-stu-id="feda0-130">Example 5: Get the container for the local developer storage account</span></span>
```
PS C:\>New-AzStorageContext -Local | Get-AzStorageContainer
```

<span data-ttu-id="feda0-131">To polecenie tworzy kontekst przy użyciu konta magazynu lokalnego rozwoju, a następnie przekazuje nowy kontekst do polecenia cmdlet **Get-AzStorageContainer** przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="feda0-131">This command creates a context by using the local development storage account, and then passes the new context to the **Get-AzStorageContainer** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="feda0-132">To polecenie pobiera kontener magazynu platformy Azure dla lokalnego konta magazynu dewelopera.</span><span class="sxs-lookup"><span data-stu-id="feda0-132">The command gets the Azure Storage container for the local developer storage account.</span></span>

### <span data-ttu-id="feda0-133">Przykład 6. Uzyskiwanie wielu kontenerów</span><span class="sxs-lookup"><span data-stu-id="feda0-133">Example 6: Get multiple containers</span></span>
```
PS C:\>$Context01 = New-AzStorageContext -Local 
PS C:\> $Context02 = New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
PS C:\> ($Context01, $Context02) | Get-AzStorageContainer
```

<span data-ttu-id="feda0-134">Pierwsze polecenie tworzy kontekst przy użyciu konta magazynu rozwoju lokalnego, a następnie przechowuje ten kontekst w zmiennej $Context 01.</span><span class="sxs-lookup"><span data-stu-id="feda0-134">The first command creates a context by using the local development storage account, and then stores that context in the $Context01 variable.</span></span>
<span data-ttu-id="feda0-135">Drugie polecenie tworzy kontekst dla konta o nazwie ContosoGeneral, które korzysta z określonego klucza, a następnie przechowuje ten kontekst w zmiennej $Context 02.</span><span class="sxs-lookup"><span data-stu-id="feda0-135">The second command creates a context for the account named ContosoGeneral that uses the specified key, and then stores that context in the $Context02 variable.</span></span>
<span data-ttu-id="feda0-136">Końcowe polecenie pobiera kontenery dla kontekstów przechowywanych w programach $Context 01 i $Context 02 za pomocą narzędzia **Get-AzStorageContainer.**</span><span class="sxs-lookup"><span data-stu-id="feda0-136">The final command gets the containers for the contexts stored in $Context01 and $Context02 by using **Get-AzStorageContainer**.</span></span>

### <span data-ttu-id="feda0-137">Przykład 7. Tworzenie kontekstu za pomocą punktu końcowego</span><span class="sxs-lookup"><span data-stu-id="feda0-137">Example 7: Create a context with an endpoint</span></span>
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Endpoint "contosoaccount.core.windows.net"
```

<span data-ttu-id="feda0-138">To polecenie tworzy kontekst magazynu platformy Azure, który ma określony punkt końcowy magazynu.</span><span class="sxs-lookup"><span data-stu-id="feda0-138">This command creates an Azure Storage context that has the specified storage endpoint.</span></span>
<span data-ttu-id="feda0-139">Polecenie tworzy kontekst dla konta o nazwie ContosoGeneral, które używa określonego klucza.</span><span class="sxs-lookup"><span data-stu-id="feda0-139">The command creates the context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="feda0-140">Przykład 8. Tworzenie kontekstu w określonym środowisku</span><span class="sxs-lookup"><span data-stu-id="feda0-140">Example 8: Create a context with a specified environment</span></span>
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Environment "AzureChinaCloud"
```

<span data-ttu-id="feda0-141">To polecenie tworzy kontekst magazynu platformy Azure, który ma określone środowisko platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="feda0-141">This command creates an Azure storage context that has the specified Azure environment.</span></span>
<span data-ttu-id="feda0-142">Polecenie tworzy kontekst dla konta o nazwie ContosoGeneral, które używa określonego klucza.</span><span class="sxs-lookup"><span data-stu-id="feda0-142">The command creates the context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="feda0-143">Przykład 9. Tworzenie kontekstu przy użyciu tokenu SAS</span><span class="sxs-lookup"><span data-stu-id="feda0-143">Example 9: Create a context by using an SAS token</span></span>
```
PS C:\>$SasToken = New-AzStorageContainerSASToken -Name "ContosoMain" -Permission "rad"
PS C:\> $Context = New-AzStorageContext -StorageAccountName "ContosoGeneral" -SasToken $SasToken
PS C:\> $Context | Get-AzStorageBlob -Container "ContosoMain"
```

<span data-ttu-id="feda0-144">Pierwsze polecenie generuje token SAS przy użyciu polecenia cmdlet **New-AzStorageContainerSASToken** dla kontenera o nazwie ContosoMain, a następnie przechowuje ten token w $SasToken danych.</span><span class="sxs-lookup"><span data-stu-id="feda0-144">The first command generates an SAS token by using the **New-AzStorageContainerSASToken** cmdlet for the container named ContosoMain, and then stores that token in the $SasToken variable.</span></span>
<span data-ttu-id="feda0-145">Token ten jest do odczytu, dodawania, aktualizowania i usuwania uprawnień.</span><span class="sxs-lookup"><span data-stu-id="feda0-145">That token is for read, add, update, and delete permissions.</span></span>
<span data-ttu-id="feda0-146">Drugie polecenie tworzy kontekst dla konta o nazwie ContosoGeneral, które używa tokenu SAS przechowywanego w programie $SasToken, a następnie przechowuje ten kontekst w $Context zmienną.</span><span class="sxs-lookup"><span data-stu-id="feda0-146">The second command creates a context for the account named ContosoGeneral that uses the SAS token stored in $SasToken, and then stores that context in the $Context variable.</span></span>
<span data-ttu-id="feda0-147">Końcowe polecenie wyświetla listę wszystkich obiektów blob skojarzonych z kontenerem o nazwie ContosoMain przy użyciu kontekstu przechowywanego w $Context.</span><span class="sxs-lookup"><span data-stu-id="feda0-147">The final command lists all the blobs associated with the container named ContosoMain by using the context stored in $Context.</span></span>

### <span data-ttu-id="feda0-148">Przykład 10. Tworzenie kontekstu przy użyciu uwierzytelniania OAuth</span><span class="sxs-lookup"><span data-stu-id="feda0-148">Example 10: Create a context by using the OAuth Authentication</span></span>
```
PS C:\>Connect-AzAccount
PS C:\> $Context = New-AzStorageContext -StorageAccountName "myaccountname" -UseConnectedAccount
```

<span data-ttu-id="feda0-149">To polecenie tworzy kontekst przy użyciu uwierzytelniania OAuth (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="feda0-149">This command creates a context by using the OAuth (Azure AD) Authentication.</span></span>

## <span data-ttu-id="feda0-150">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="feda0-150">PARAMETERS</span></span>

### <span data-ttu-id="feda0-151">— Anonimowe</span><span class="sxs-lookup"><span data-stu-id="feda0-151">-Anonymous</span></span>
<span data-ttu-id="feda0-152">Wskazuje, że to polecenie cmdlet tworzy kontekst magazynu platformy Azure dla logowania anonimowego.</span><span class="sxs-lookup"><span data-stu-id="feda0-152">Indicates that this cmdlet creates an Azure Storage context for anonymous logon.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AnonymousAccount, AnonymousAccountEnvironment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="feda0-153">- ConnectionString</span><span class="sxs-lookup"><span data-stu-id="feda0-153">-ConnectionString</span></span>
<span data-ttu-id="feda0-154">Określa ciąg połączenia dla kontekstu magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="feda0-154">Specifies a connection string for the Azure Storage context.</span></span>

```yaml
Type: System.String
Parameter Sets: ConnectionString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="feda0-155">- Punkt końcowy</span><span class="sxs-lookup"><span data-stu-id="feda0-155">-Endpoint</span></span>
<span data-ttu-id="feda0-156">Określa punkt końcowy dla kontekstu magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="feda0-156">Specifies the endpoint for the Azure Storage context.</span></span>

```yaml
Type: System.String
Parameter Sets: OAuthAccount, AccountNameAndKey, AnonymousAccount, SasToken
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="feda0-157">— Środowisko</span><span class="sxs-lookup"><span data-stu-id="feda0-157">-Environment</span></span>
<span data-ttu-id="feda0-158">Określa środowisko platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="feda0-158">Specifies the Azure environment.</span></span>
<span data-ttu-id="feda0-159">Dopuszczalne wartości dla tego parametru to: AzureCloud i AzureChinaCloud.</span><span class="sxs-lookup"><span data-stu-id="feda0-159">The acceptable values for this parameter are: AzureCloud and AzureChinaCloud.</span></span>
<span data-ttu-id="feda0-160">Aby uzyskać więcej informacji, wpisz `Get-Help Get-AzEnvironment` .</span><span class="sxs-lookup"><span data-stu-id="feda0-160">For more information, type `Get-Help Get-AzEnvironment`.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameAndKeyEnvironment, AnonymousAccountEnvironment
Aliases: Name, EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SasTokenWithAzureEnvironment, OAuthAccountEnvironment
Aliases: Name, EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="feda0-161">— Lokalny</span><span class="sxs-lookup"><span data-stu-id="feda0-161">-Local</span></span>
<span data-ttu-id="feda0-162">Wskazuje, że to polecenie cmdlet tworzy kontekst przy użyciu konta magazynu dla rozwoju lokalnego.</span><span class="sxs-lookup"><span data-stu-id="feda0-162">Indicates that this cmdlet creates a context by using the local development storage account.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: LocalDevelopment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="feda0-163">— Protokół</span><span class="sxs-lookup"><span data-stu-id="feda0-163">-Protocol</span></span>
<span data-ttu-id="feda0-164">Transfer Protocol (https/http).</span><span class="sxs-lookup"><span data-stu-id="feda0-164">Transfer Protocol (https/http).</span></span>

```yaml
Type: System.String
Parameter Sets: OAuthAccount, AccountNameAndKey, AccountNameAndKeyEnvironment, AnonymousAccount, AnonymousAccountEnvironment, SasToken, OAuthAccountEnvironment
Aliases:
Accepted values: Http, Https

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="feda0-165">- SasToken</span><span class="sxs-lookup"><span data-stu-id="feda0-165">-SasToken</span></span>
<span data-ttu-id="feda0-166">Określa token SAS (Shared Access Signature) dla kontekstu.</span><span class="sxs-lookup"><span data-stu-id="feda0-166">Specifies a Shared Access Signature (SAS) token for the context.</span></span>

```yaml
Type: System.String
Parameter Sets: SasToken, SasTokenWithAzureEnvironment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="feda0-167">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="feda0-167">-StorageAccountKey</span></span>
<span data-ttu-id="feda0-168">Określa klucz konta magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="feda0-168">Specifies an Azure Storage account key.</span></span>
<span data-ttu-id="feda0-169">To polecenie cmdlet tworzy kontekst dla klucza, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="feda0-169">This cmdlet creates a context for the key that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameAndKey, AccountNameAndKeyEnvironment
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="feda0-170">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="feda0-170">-StorageAccountName</span></span>
<span data-ttu-id="feda0-171">Określa nazwę konta magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="feda0-171">Specifies an Azure Storage account name.</span></span>
<span data-ttu-id="feda0-172">To polecenie cmdlet tworzy kontekst dla konta, które określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="feda0-172">This cmdlet creates a context for the account that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: OAuthAccount, AccountNameAndKey, AccountNameAndKeyEnvironment, AnonymousAccount, AnonymousAccountEnvironment, SasToken, SasTokenWithAzureEnvironment, OAuthAccountEnvironment
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="feda0-173">—UseConnectedAccount</span><span class="sxs-lookup"><span data-stu-id="feda0-173">-UseConnectedAccount</span></span>
<span data-ttu-id="feda0-174">Wskazuje, że to polecenie cmdlet tworzy kontekst magazynu platformy Azure za pomocą uwierzytelniania OAuth (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="feda0-174">Indicates that this cmdlet creates an Azure Storage context with OAuth (Azure AD) Authentication.</span></span>
<span data-ttu-id="feda0-175">Polecenie cmdlet domyślnie używa uwierzytelniania OAuth, gdy inne uwierzytelnianie nie zostanie określone.</span><span class="sxs-lookup"><span data-stu-id="feda0-175">The cmdlet will use OAuth Authentication by default, when other authentication not specified.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: OAuthAccount, OAuthAccountEnvironment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="feda0-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="feda0-176">CommonParameters</span></span>
<span data-ttu-id="feda0-177">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="feda0-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="feda0-178">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="feda0-178">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="feda0-179">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="feda0-179">INPUTS</span></span>

### <span data-ttu-id="feda0-180">System.String</span><span class="sxs-lookup"><span data-stu-id="feda0-180">System.String</span></span>

## <span data-ttu-id="feda0-181">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="feda0-181">OUTPUTS</span></span>

### <span data-ttu-id="feda0-182">Microsoft.WindowsAzure.Commands.Storage.AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="feda0-182">Microsoft.WindowsAzure.Commands.Storage.AzureStorageContext</span></span>

## <span data-ttu-id="feda0-183">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="feda0-183">NOTES</span></span>

## <span data-ttu-id="feda0-184">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="feda0-184">RELATED LINKS</span></span>

[<span data-ttu-id="feda0-185">Get-AzstorageBlob</span><span class="sxs-lookup"><span data-stu-id="feda0-185">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="feda0-186">New-AzstorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="feda0-186">New-AzStorageContainerSASToken</span></span>](./New-AzStorageContainerSASToken.md)


