---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 383402B2-6B7C-41AB-AFF9-36C86156B0A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragecontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContext.md
ms.openlocfilehash: ae12bb509773f36ecfd94ad6907499f0b5feb02d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93895537"
---
# <span data-ttu-id="6f95b-101">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="6f95b-101">New-AzStorageContext</span></span>

## <span data-ttu-id="6f95b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6f95b-102">SYNOPSIS</span></span>
<span data-ttu-id="6f95b-103">Tworzy kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="6f95b-103">Creates an Azure Storage context.</span></span>

## <span data-ttu-id="6f95b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6f95b-104">SYNTAX</span></span>

### <span data-ttu-id="6f95b-105">OAuthAccount (domyślny)</span><span class="sxs-lookup"><span data-stu-id="6f95b-105">OAuthAccount (Default)</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-UseConnectedAccount] [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="6f95b-106">AccountNameAndKey</span><span class="sxs-lookup"><span data-stu-id="6f95b-106">AccountNameAndKey</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="6f95b-107">AccountNameAndKeyEnvironment</span><span class="sxs-lookup"><span data-stu-id="6f95b-107">AccountNameAndKeyEnvironment</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 -Environment <String> [<CommonParameters>]
```

### <span data-ttu-id="6f95b-108">AnonymousAccount</span><span class="sxs-lookup"><span data-stu-id="6f95b-108">AnonymousAccount</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] [-Endpoint <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="6f95b-109">AnonymousAccountEnvironment</span><span class="sxs-lookup"><span data-stu-id="6f95b-109">AnonymousAccountEnvironment</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] -Environment <String>
 [<CommonParameters>]
```

### <span data-ttu-id="6f95b-110">SasToken</span><span class="sxs-lookup"><span data-stu-id="6f95b-110">SasToken</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> -SasToken <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="6f95b-111">SasTokenWithAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="6f95b-111">SasTokenWithAzureEnvironment</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> -SasToken <String> -Environment <String>
 [<CommonParameters>]
```

### <span data-ttu-id="6f95b-112">OAuthAccountEnvironment</span><span class="sxs-lookup"><span data-stu-id="6f95b-112">OAuthAccountEnvironment</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-UseConnectedAccount] [-Protocol <String>]
 -Environment <String> [<CommonParameters>]
```

### <span data-ttu-id="6f95b-113">Elemencie</span><span class="sxs-lookup"><span data-stu-id="6f95b-113">ConnectionString</span></span>
```
New-AzStorageContext -ConnectionString <String> [<CommonParameters>]
```

### <span data-ttu-id="6f95b-114">LocalDevelopment</span><span class="sxs-lookup"><span data-stu-id="6f95b-114">LocalDevelopment</span></span>
```
New-AzStorageContext [-Local] [<CommonParameters>]
```

## <span data-ttu-id="6f95b-115">Opis</span><span class="sxs-lookup"><span data-stu-id="6f95b-115">DESCRIPTION</span></span>
<span data-ttu-id="6f95b-116">Polecenie cmdlet **New-AzStorageContext** umożliwia utworzenie kontekstu usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="6f95b-116">The **New-AzStorageContext** cmdlet creates an Azure Storage context.</span></span>
<span data-ttu-id="6f95b-117">Domyślnym uwierzytelnianiem kontekstu magazynu jest OAuth (Azure AD), jeśli jest dostępna tylko nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="6f95b-117">The default Authentication of a Storage Context is OAuth (Azure AD), if only input Storage account name.</span></span>
<span data-ttu-id="6f95b-118">Zobacz szczegóły uwierzytelniania usługi magazynu https://docs.microsoft.com/en-us/rest/api/storageservices/authorization-for-the-azure-storage-services .</span><span class="sxs-lookup"><span data-stu-id="6f95b-118">See details of authentication of the Storage Service in https://docs.microsoft.com/en-us/rest/api/storageservices/authorization-for-the-azure-storage-services.</span></span>

## <span data-ttu-id="6f95b-119">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6f95b-119">EXAMPLES</span></span>

### <span data-ttu-id="6f95b-120">Przykład 1. Tworzenie kontekstu przez określenie nazwy i klucza konta magazynu</span><span class="sxs-lookup"><span data-stu-id="6f95b-120">Example 1: Create a context by specifying a storage account name and key</span></span>
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
```

<span data-ttu-id="6f95b-121">To polecenie tworzy kontekst dla konta o nazwie ContosoGeneral, który używa określonego klucza.</span><span class="sxs-lookup"><span data-stu-id="6f95b-121">This command creates a context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="6f95b-122">Przykład 2: Tworzenie kontekstu przez określenie parametrów połączenia</span><span class="sxs-lookup"><span data-stu-id="6f95b-122">Example 2: Create a context by specifying a connection string</span></span>
```
PS C:\>New-AzStorageContext -ConnectionString "DefaultEndpointsProtocol=https;AccountName=ContosoGeneral;AccountKey=< Storage Key for ContosoGeneral ends with == >;"
```

<span data-ttu-id="6f95b-123">To polecenie tworzy kontekst na podstawie określonych parametrów połączenia dla konta ContosoGeneral.</span><span class="sxs-lookup"><span data-stu-id="6f95b-123">This command creates a context based on the specified connection string for the account ContosoGeneral.</span></span>

### <span data-ttu-id="6f95b-124">Przykład 3: Tworzenie kontekstu dla konta magazynu anonimowego</span><span class="sxs-lookup"><span data-stu-id="6f95b-124">Example 3: Create a context for an anonymous storage account</span></span>
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -Anonymous -Protocol "http"
```

<span data-ttu-id="6f95b-125">To polecenie tworzy kontekst do anonimowego korzystania z konta o nazwie ContosoGeneral.</span><span class="sxs-lookup"><span data-stu-id="6f95b-125">This command creates a context for anonymous use for the account named ContosoGeneral.</span></span>
<span data-ttu-id="6f95b-126">To polecenie określa HTTP jako protokół połączenia.</span><span class="sxs-lookup"><span data-stu-id="6f95b-126">The command specifies HTTP as a connection protocol.</span></span>

### <span data-ttu-id="6f95b-127">Przykład 4: Tworzenie kontekstu za pomocą lokalnego konta magazynu opracowywania</span><span class="sxs-lookup"><span data-stu-id="6f95b-127">Example 4: Create a context by using the local development storage account</span></span>
```
PS C:\>New-AzStorageContext -Local
```

<span data-ttu-id="6f95b-128">To polecenie tworzy kontekst za pomocą lokalnego konta magazynu dla deweloperów.</span><span class="sxs-lookup"><span data-stu-id="6f95b-128">This command creates a context by using the local development storage account.</span></span>
<span data-ttu-id="6f95b-129">Polecenie określa parametr *Local* .</span><span class="sxs-lookup"><span data-stu-id="6f95b-129">The command specifies the *Local* parameter.</span></span>

### <span data-ttu-id="6f95b-130">Przykład 5: uzyskiwanie kontenera dla lokalnego konta magazynu dewelopera</span><span class="sxs-lookup"><span data-stu-id="6f95b-130">Example 5: Get the container for the local developer storage account</span></span>
```
PS C:\>New-AzStorageContext -Local | Get-AzStorageContainer
```

<span data-ttu-id="6f95b-131">To polecenie tworzy kontekst przy użyciu lokalnego konta magazynu dla programistów, a następnie przekazuje nowy kontekst do polecenia cmdlet **Get-AzStorageContainer** przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="6f95b-131">This command creates a context by using the local development storage account, and then passes the new context to the **Get-AzStorageContainer** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="6f95b-132">Polecenie pobiera kontener magazynu platformy Azure dla konta magazynu lokalnego dla deweloperów.</span><span class="sxs-lookup"><span data-stu-id="6f95b-132">The command gets the Azure Storage container for the local developer storage account.</span></span>

### <span data-ttu-id="6f95b-133">Przykład 6: uzyskiwanie wielu kontenerów</span><span class="sxs-lookup"><span data-stu-id="6f95b-133">Example 6: Get multiple containers</span></span>
```
PS C:\>$Context01 = New-AzStorageContext -Local 
PS C:\> $Context02 = New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
PS C:\> ($Context01, $Context02) | Get-AzStorageContainer
```

<span data-ttu-id="6f95b-134">Pierwsze polecenie tworzy kontekst przy użyciu lokalnego konta magazynu dla programistów, a następnie przechowuje ten kontekst w zmiennej $Context 01.</span><span class="sxs-lookup"><span data-stu-id="6f95b-134">The first command creates a context by using the local development storage account, and then stores that context in the $Context01 variable.</span></span>
<span data-ttu-id="6f95b-135">Drugie polecenie tworzy kontekst dla konta o nazwie ContosoGeneral, który używa określonego klucza, a następnie zapisuje ten kontekst w zmiennej $Context 02.</span><span class="sxs-lookup"><span data-stu-id="6f95b-135">The second command creates a context for the account named ContosoGeneral that uses the specified key, and then stores that context in the $Context02 variable.</span></span>
<span data-ttu-id="6f95b-136">Polecenie ostatnie uzyskuje kontenery dla kontekstów przechowywanych w $Context 01 i $Context 02 przy użyciu polecenia **Get-AzStorageContainer**.</span><span class="sxs-lookup"><span data-stu-id="6f95b-136">The final command gets the containers for the contexts stored in $Context01 and $Context02 by using **Get-AzStorageContainer**.</span></span>

### <span data-ttu-id="6f95b-137">Przykład 7: Tworzenie kontekstu za pomocą punktu końcowego</span><span class="sxs-lookup"><span data-stu-id="6f95b-137">Example 7: Create a context with an endpoint</span></span>
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Endpoint "contosoaccount.core.windows.net"
```

<span data-ttu-id="6f95b-138">To polecenie tworzy kontekst usługi Azure Storage o określonym punkcie końcowym magazynu.</span><span class="sxs-lookup"><span data-stu-id="6f95b-138">This command creates an Azure Storage context that has the specified storage endpoint.</span></span>
<span data-ttu-id="6f95b-139">Polecenie utworzy kontekst dla konta o nazwie ContosoGeneral, który używa określonego klucza.</span><span class="sxs-lookup"><span data-stu-id="6f95b-139">The command creates the context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="6f95b-140">Przykład 8: Tworzenie kontekstu za pomocą określonego środowiska</span><span class="sxs-lookup"><span data-stu-id="6f95b-140">Example 8: Create a context with a specified environment</span></span>
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Environment "AzureChinaCloud"
```

<span data-ttu-id="6f95b-141">To polecenie tworzy kontekst usługi Azure Storage z określonym środowiskiem platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6f95b-141">This command creates an Azure storage context that has the specified Azure environment.</span></span>
<span data-ttu-id="6f95b-142">Polecenie utworzy kontekst dla konta o nazwie ContosoGeneral, który używa określonego klucza.</span><span class="sxs-lookup"><span data-stu-id="6f95b-142">The command creates the context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="6f95b-143">Przykład 9: Tworzenie kontekstu za pomocą tokenu SAS</span><span class="sxs-lookup"><span data-stu-id="6f95b-143">Example 9: Create a context by using an SAS token</span></span>
```
PS C:\>$SasToken = New-AzStorageContainerSASToken -Name "ContosoMain" -Permission "rad"
PS C:\> $Context = New-AzStorageContext -StorageAccountName "ContosoGeneral" -SasToken $SasToken
PS C:\> $Context | Get-AzStorageBlob -Container "ContosoMain"
```

<span data-ttu-id="6f95b-144">Pierwsze polecenie generuje token SAS przy użyciu polecenia cmdlet **New-AzStorageContainerSASToken** dla kontenera o nazwie ContosoMain, a następnie zapisuje ten token w zmiennej $SasToken.</span><span class="sxs-lookup"><span data-stu-id="6f95b-144">The first command generates an SAS token by using the **New-AzStorageContainerSASToken** cmdlet for the container named ContosoMain, and then stores that token in the $SasToken variable.</span></span>
<span data-ttu-id="6f95b-145">Token ten jest przeznaczony dla uprawnień Odczyt, Dodawanie, aktualizowanie i usuwanie.</span><span class="sxs-lookup"><span data-stu-id="6f95b-145">That token is for read, add, update, and delete permissions.</span></span>
<span data-ttu-id="6f95b-146">Drugie polecenie tworzy kontekst dla konta o nazwie ContosoGeneral, w którym jest używany token SAS przechowywany w $SasToken, a następnie przechowuje ten kontekst w zmiennej $Context.</span><span class="sxs-lookup"><span data-stu-id="6f95b-146">The second command creates a context for the account named ContosoGeneral that uses the SAS token stored in $SasToken, and then stores that context in the $Context variable.</span></span>
<span data-ttu-id="6f95b-147">W ostatnim poleceniu są wyświetlane wszystkie obiekty blob skojarzone z kontenerem o nazwie ContosoMain przy użyciu kontekstu przechowywanego w $Context.</span><span class="sxs-lookup"><span data-stu-id="6f95b-147">The final command lists all the blobs associated with the container named ContosoMain by using the context stored in $Context.</span></span>

### <span data-ttu-id="6f95b-148">Przykład 10: Tworzenie kontekstu przy użyciu uwierzytelniania OAuth</span><span class="sxs-lookup"><span data-stu-id="6f95b-148">Example 10: Create a context by using the OAuth Authentication</span></span>
```
PS C:\>Connect-AzAccount
PS C:\> $Context = New-AzStorageContext -StorageAccountName "myaccountname" -UseConnectedAccount
```

<span data-ttu-id="6f95b-149">To polecenie tworzy kontekst przy użyciu uwierzytelniania OAuth (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="6f95b-149">This command creates a context by using the OAuth (Azure AD) Authentication.</span></span>

## <span data-ttu-id="6f95b-150">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6f95b-150">PARAMETERS</span></span>

### <span data-ttu-id="6f95b-151">-Anonymous</span><span class="sxs-lookup"><span data-stu-id="6f95b-151">-Anonymous</span></span>
<span data-ttu-id="6f95b-152">Wskazuje, że to polecenie cmdlet tworzy kontekst usługi Azure Storage do logowania anonimowego.</span><span class="sxs-lookup"><span data-stu-id="6f95b-152">Indicates that this cmdlet creates an Azure Storage context for anonymous logon.</span></span>

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

### <span data-ttu-id="6f95b-153">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="6f95b-153">-ConnectionString</span></span>
<span data-ttu-id="6f95b-154">Określa parametry połączenia dla kontekstu usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="6f95b-154">Specifies a connection string for the Azure Storage context.</span></span>

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

### <span data-ttu-id="6f95b-155">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="6f95b-155">-Endpoint</span></span>
<span data-ttu-id="6f95b-156">Określa punkt końcowy kontekstu usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="6f95b-156">Specifies the endpoint for the Azure Storage context.</span></span>

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

### <span data-ttu-id="6f95b-157">-Środowisko</span><span class="sxs-lookup"><span data-stu-id="6f95b-157">-Environment</span></span>
<span data-ttu-id="6f95b-158">Określa środowisko Azure.</span><span class="sxs-lookup"><span data-stu-id="6f95b-158">Specifies the Azure environment.</span></span>
<span data-ttu-id="6f95b-159">Dopuszczalne wartości tego parametru to: AzureCloud oraz AzureChinaCloud.</span><span class="sxs-lookup"><span data-stu-id="6f95b-159">The acceptable values for this parameter are: AzureCloud and AzureChinaCloud.</span></span>
<span data-ttu-id="6f95b-160">Aby uzyskać więcej informacji, wpisz tekst `Get-Help Get-AzEnvironment` .</span><span class="sxs-lookup"><span data-stu-id="6f95b-160">For more information, type `Get-Help Get-AzEnvironment`.</span></span>

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

### <span data-ttu-id="6f95b-161">-Local</span><span class="sxs-lookup"><span data-stu-id="6f95b-161">-Local</span></span>
<span data-ttu-id="6f95b-162">Wskazuje, że to polecenie cmdlet tworzy kontekst przy użyciu lokalnego konta magazynu dla deweloperów.</span><span class="sxs-lookup"><span data-stu-id="6f95b-162">Indicates that this cmdlet creates a context by using the local development storage account.</span></span>

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

### <span data-ttu-id="6f95b-163">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="6f95b-163">-Protocol</span></span>
<span data-ttu-id="6f95b-164">Protokół transferu (https/http).</span><span class="sxs-lookup"><span data-stu-id="6f95b-164">Transfer Protocol (https/http).</span></span>

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

### <span data-ttu-id="6f95b-165">-SasToken</span><span class="sxs-lookup"><span data-stu-id="6f95b-165">-SasToken</span></span>
<span data-ttu-id="6f95b-166">Określa token funkcji dostępu współużytkowanego (SAS, Access Signature) dla kontekstu.</span><span class="sxs-lookup"><span data-stu-id="6f95b-166">Specifies a Shared Access Signature (SAS) token for the context.</span></span>

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

### <span data-ttu-id="6f95b-167">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="6f95b-167">-StorageAccountKey</span></span>
<span data-ttu-id="6f95b-168">Określa klucz konta usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="6f95b-168">Specifies an Azure Storage account key.</span></span>
<span data-ttu-id="6f95b-169">To polecenie cmdlet tworzy kontekst dla klucza, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="6f95b-169">This cmdlet creates a context for the key that this parameter specifies.</span></span>

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

### <span data-ttu-id="6f95b-170">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="6f95b-170">-StorageAccountName</span></span>
<span data-ttu-id="6f95b-171">Określa nazwę konta magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6f95b-171">Specifies an Azure Storage account name.</span></span>
<span data-ttu-id="6f95b-172">To polecenie cmdlet tworzy kontekst dla konta, które określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="6f95b-172">This cmdlet creates a context for the account that this parameter specifies.</span></span>

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

### <span data-ttu-id="6f95b-173">-UseConnectedAccount</span><span class="sxs-lookup"><span data-stu-id="6f95b-173">-UseConnectedAccount</span></span>
<span data-ttu-id="6f95b-174">Wskazuje, że to polecenie cmdlet tworzy kontekst usługi Azure Storage z uwierzytelnianiem OAuth (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="6f95b-174">Indicates that this cmdlet creates an Azure Storage context with OAuth (Azure AD) Authentication.</span></span>
<span data-ttu-id="6f95b-175">Polecenie cmdlet będzie domyślnie używać uwierzytelniania OAuth, jeśli nie podano innego uwierzytelniania.</span><span class="sxs-lookup"><span data-stu-id="6f95b-175">The cmdlet will use OAuth Authentication by default, when other authentication not specified.</span></span>

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

### <span data-ttu-id="6f95b-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f95b-176">CommonParameters</span></span>
<span data-ttu-id="6f95b-177">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f95b-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f95b-178">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f95b-178">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f95b-179">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6f95b-179">INPUTS</span></span>

### <span data-ttu-id="6f95b-180">System. String</span><span class="sxs-lookup"><span data-stu-id="6f95b-180">System.String</span></span>

## <span data-ttu-id="6f95b-181">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6f95b-181">OUTPUTS</span></span>

### <span data-ttu-id="6f95b-182">Microsoft. platformy windowsazure. Commands. Storage. AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="6f95b-182">Microsoft.WindowsAzure.Commands.Storage.AzureStorageContext</span></span>

## <span data-ttu-id="6f95b-183">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6f95b-183">NOTES</span></span>

## <span data-ttu-id="6f95b-184">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6f95b-184">RELATED LINKS</span></span>

[<span data-ttu-id="6f95b-185">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="6f95b-185">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="6f95b-186">Nowe — AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="6f95b-186">New-AzStorageContainerSASToken</span></span>](./New-AzStorageContainerSASToken.md)


