---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 383402B2-6B7C-41AB-AFF9-36C86156B0A9
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragecontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageContext.md
ms.openlocfilehash: 9de6b2b52205bdf80de9c57e3e338f4b7216c5ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547784"
---
# <span data-ttu-id="bf4b7-101">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="bf4b7-101">New-AzureStorageContext</span></span>

## <span data-ttu-id="bf4b7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bf4b7-102">SYNOPSIS</span></span>
<span data-ttu-id="bf4b7-103">Tworzy kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="bf4b7-103">Creates an Azure Storage context.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bf4b7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bf4b7-104">SYNTAX</span></span>

### <span data-ttu-id="bf4b7-105">OAuthAccount (domyślny)</span><span class="sxs-lookup"><span data-stu-id="bf4b7-105">OAuthAccount (Default)</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> [-UseConnectedAccount] [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="bf4b7-106">AccountNameAndKey</span><span class="sxs-lookup"><span data-stu-id="bf4b7-106">AccountNameAndKey</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="bf4b7-107">AccountNameAndKeyEnvironment</span><span class="sxs-lookup"><span data-stu-id="bf4b7-107">AccountNameAndKeyEnvironment</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 -Environment <String> [<CommonParameters>]
```

### <span data-ttu-id="bf4b7-108">AnonymousAccount</span><span class="sxs-lookup"><span data-stu-id="bf4b7-108">AnonymousAccount</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] [-Endpoint <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="bf4b7-109">AnonymousAccountEnvironment</span><span class="sxs-lookup"><span data-stu-id="bf4b7-109">AnonymousAccountEnvironment</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] -Environment <String>
 [<CommonParameters>]
```

### <span data-ttu-id="bf4b7-110">SasToken</span><span class="sxs-lookup"><span data-stu-id="bf4b7-110">SasToken</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> -SasToken <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="bf4b7-111">SasTokenWithAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="bf4b7-111">SasTokenWithAzureEnvironment</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> -SasToken <String> -Environment <String>
 [<CommonParameters>]
```

### <span data-ttu-id="bf4b7-112">OAuthAccountEnvironment</span><span class="sxs-lookup"><span data-stu-id="bf4b7-112">OAuthAccountEnvironment</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> [-UseConnectedAccount] [-Protocol <String>]
 -Environment <String> [<CommonParameters>]
```

### <span data-ttu-id="bf4b7-113">Elemencie</span><span class="sxs-lookup"><span data-stu-id="bf4b7-113">ConnectionString</span></span>
```
New-AzureStorageContext -ConnectionString <String> [<CommonParameters>]
```

### <span data-ttu-id="bf4b7-114">LocalDevelopment</span><span class="sxs-lookup"><span data-stu-id="bf4b7-114">LocalDevelopment</span></span>
```
New-AzureStorageContext [-Local] [<CommonParameters>]
```

## <span data-ttu-id="bf4b7-115">Opis</span><span class="sxs-lookup"><span data-stu-id="bf4b7-115">DESCRIPTION</span></span>
<span data-ttu-id="bf4b7-116">Polecenie cmdlet **New-AzureStorageContext** umożliwia utworzenie kontekstu usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="bf4b7-116">The **New-AzureStorageContext** cmdlet creates an Azure Storage context.</span></span>

## <span data-ttu-id="bf4b7-117">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bf4b7-117">EXAMPLES</span></span>

### <span data-ttu-id="bf4b7-118">Przykład 1. Tworzenie kontekstu przez określenie nazwy i klucza konta magazynu</span><span class="sxs-lookup"><span data-stu-id="bf4b7-118">Example 1: Create a context by specifying a storage account name and key</span></span>
```
C:\PS>New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
```

<span data-ttu-id="bf4b7-119">To polecenie tworzy kontekst dla konta o nazwie ContosoGeneral, który używa określonego klucza.</span><span class="sxs-lookup"><span data-stu-id="bf4b7-119">This command creates a context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="bf4b7-120">Przykład 2: Tworzenie kontekstu przez określenie parametrów połączenia</span><span class="sxs-lookup"><span data-stu-id="bf4b7-120">Example 2: Create a context by specifying a connection string</span></span>
```
C:\PS>New-AzureStorageContext -ConnectionString "DefaultEndpointsProtocol=https;AccountName=ContosoGeneral;AccountKey=< Storage Key for ContosoGeneral ends with == >;"
```

<span data-ttu-id="bf4b7-121">To polecenie tworzy kontekst na podstawie określonych parametrów połączenia dla konta ContosoGeneral.</span><span class="sxs-lookup"><span data-stu-id="bf4b7-121">This command creates a context based on the specified connection string for the account ContosoGeneral.</span></span>

### <span data-ttu-id="bf4b7-122">Przykład 3: Tworzenie kontekstu dla konta magazynu anonimowego</span><span class="sxs-lookup"><span data-stu-id="bf4b7-122">Example 3: Create a context for an anonymous storage account</span></span>
```
C:\PS>New-AzureStorageContext -StorageAccountName "ContosoGeneral" -Anonymous -Protocol "http"
```

<span data-ttu-id="bf4b7-123">To polecenie tworzy kontekst do anonimowego korzystania z konta o nazwie ContosoGeneral.</span><span class="sxs-lookup"><span data-stu-id="bf4b7-123">This command creates a context for anonymous use for the account named ContosoGeneral.</span></span>
<span data-ttu-id="bf4b7-124">To polecenie określa HTTP jako protokół połączenia.</span><span class="sxs-lookup"><span data-stu-id="bf4b7-124">The command specifies HTTP as a connection protocol.</span></span>

### <span data-ttu-id="bf4b7-125">Przykład 4: Tworzenie kontekstu za pomocą lokalnego konta magazynu opracowywania</span><span class="sxs-lookup"><span data-stu-id="bf4b7-125">Example 4: Create a context by using the local development storage account</span></span>
```
C:\PS>New-AzureStorageContext -Local
```

<span data-ttu-id="bf4b7-126">To polecenie tworzy kontekst za pomocą lokalnego konta magazynu dla deweloperów.</span><span class="sxs-lookup"><span data-stu-id="bf4b7-126">This command creates a context by using the local development storage account.</span></span>
<span data-ttu-id="bf4b7-127">Polecenie określa parametr *Local* .</span><span class="sxs-lookup"><span data-stu-id="bf4b7-127">The command specifies the *Local* parameter.</span></span>

### <span data-ttu-id="bf4b7-128">Przykład 5: uzyskiwanie kontenera dla lokalnego konta magazynu dewelopera</span><span class="sxs-lookup"><span data-stu-id="bf4b7-128">Example 5: Get the container for the local developer storage account</span></span>
```
C:\PS>New-AzureStorageContext -Local | Get-AzureStorageContainer
```

<span data-ttu-id="bf4b7-129">To polecenie tworzy kontekst przy użyciu lokalnego konta magazynu dla programistów, a następnie przekazuje nowy kontekst do polecenia cmdlet **Get-AzureStorageContainer** przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="bf4b7-129">This command creates a context by using the local development storage account, and then passes the new context to the **Get-AzureStorageContainer** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="bf4b7-130">Polecenie pobiera kontener magazynu platformy Azure dla konta magazynu lokalnego dla deweloperów.</span><span class="sxs-lookup"><span data-stu-id="bf4b7-130">The command gets the Azure Storage container for the local developer storage account.</span></span>

### <span data-ttu-id="bf4b7-131">Przykład 6: uzyskiwanie wielu kontenerów</span><span class="sxs-lookup"><span data-stu-id="bf4b7-131">Example 6: Get multiple containers</span></span>
```
C:\PS>$Context01 = New-AzureStorageContext -Local 
PS C:\> $Context02 = New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
PS C:\> ($Context01, $Context02) | Get-AzureStorageContainer
```

<span data-ttu-id="bf4b7-132">Pierwsze polecenie tworzy kontekst przy użyciu lokalnego konta magazynu dla programistów, a następnie przechowuje ten kontekst w zmiennej $Context 01.</span><span class="sxs-lookup"><span data-stu-id="bf4b7-132">The first command creates a context by using the local development storage account, and then stores that context in the $Context01 variable.</span></span>
<span data-ttu-id="bf4b7-133">Drugie polecenie tworzy kontekst dla konta o nazwie ContosoGeneral, który używa określonego klucza, a następnie zapisuje ten kontekst w zmiennej $Context 02.</span><span class="sxs-lookup"><span data-stu-id="bf4b7-133">The second command creates a context for the account named ContosoGeneral that uses the specified key, and then stores that context in the $Context02 variable.</span></span>
<span data-ttu-id="bf4b7-134">Polecenie ostatnie uzyskuje kontenery dla kontekstów przechowywanych w $Context 01 i $Context 02 przy użyciu polecenia **Get-AzureStorageContainer**.</span><span class="sxs-lookup"><span data-stu-id="bf4b7-134">The final command gets the containers for the contexts stored in $Context01 and $Context02 by using **Get-AzureStorageContainer**.</span></span>

### <span data-ttu-id="bf4b7-135">Przykład 7: Tworzenie kontekstu za pomocą punktu końcowego</span><span class="sxs-lookup"><span data-stu-id="bf4b7-135">Example 7: Create a context with an endpoint</span></span>
```
C:\PS>New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Endpoint "contosoaccount.core.windows.net"
```

<span data-ttu-id="bf4b7-136">To polecenie tworzy kontekst usługi Azure Storage o określonym punkcie końcowym magazynu.</span><span class="sxs-lookup"><span data-stu-id="bf4b7-136">This command creates an Azure Storage context that has the specified storage endpoint.</span></span>
<span data-ttu-id="bf4b7-137">Polecenie utworzy kontekst dla konta o nazwie ContosoGeneral, który używa określonego klucza.</span><span class="sxs-lookup"><span data-stu-id="bf4b7-137">The command creates the context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="bf4b7-138">Przykład 8: Tworzenie kontekstu za pomocą określonego środowiska</span><span class="sxs-lookup"><span data-stu-id="bf4b7-138">Example 8: Create a context with a specified environment</span></span>
```
C:\PS>New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Environment "AzureChinaCloud"
```

<span data-ttu-id="bf4b7-139">To polecenie tworzy kontekst usługi Azure Storage z określonym środowiskiem platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="bf4b7-139">This command creates an Azure storage context that has the specified Azure environment.</span></span>
<span data-ttu-id="bf4b7-140">Polecenie utworzy kontekst dla konta o nazwie ContosoGeneral, który używa określonego klucza.</span><span class="sxs-lookup"><span data-stu-id="bf4b7-140">The command creates the context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="bf4b7-141">Przykład 9: Tworzenie kontekstu za pomocą tokenu SAS</span><span class="sxs-lookup"><span data-stu-id="bf4b7-141">Example 9: Create a context by using an SAS token</span></span>
```
C:\PS>$SasToken = New-AzureStorageContainerSASToken -Name "ContosoMain" -Permission "rad"
PS C:\> $Context = New-AzureStorageContext -StorageAccountName "ContosoGeneral" -SasToken $SasToken
PS C:\> $Context | Get-AzureStorageBlob -Container "ContosoMain"
```

<span data-ttu-id="bf4b7-142">Pierwsze polecenie generuje token SAS przy użyciu polecenia cmdlet **New-AzureStorageContainerSASToken** dla kontenera o nazwie ContosoMain, a następnie zapisuje ten token w zmiennej $SasToken.</span><span class="sxs-lookup"><span data-stu-id="bf4b7-142">The first command generates an SAS token by using the **New-AzureStorageContainerSASToken** cmdlet for the container named ContosoMain, and then stores that token in the $SasToken variable.</span></span>
<span data-ttu-id="bf4b7-143">Token ten jest przeznaczony dla uprawnień Odczyt, Dodawanie, aktualizowanie i usuwanie.</span><span class="sxs-lookup"><span data-stu-id="bf4b7-143">That token is for read, add, update, and delete permissions.</span></span>
<span data-ttu-id="bf4b7-144">Drugie polecenie tworzy kontekst dla konta o nazwie ContosoGeneral, w którym jest używany token SAS przechowywany w $SasToken, a następnie przechowuje ten kontekst w zmiennej $Context.</span><span class="sxs-lookup"><span data-stu-id="bf4b7-144">The second command creates a context for the account named ContosoGeneral that uses the SAS token stored in $SasToken, and then stores that context in the $Context variable.</span></span>
<span data-ttu-id="bf4b7-145">W ostatnim poleceniu są wyświetlane wszystkie obiekty blob skojarzone z kontenerem o nazwie ContosoMain przy użyciu kontekstu przechowywanego w $Context.</span><span class="sxs-lookup"><span data-stu-id="bf4b7-145">The final command lists all the blobs associated with the container named ContosoMain by using the context stored in $Context.</span></span>

### <span data-ttu-id="bf4b7-146">Przykład 10: Tworzenie kontekstu przy użyciu uwierzytelniania OAuth</span><span class="sxs-lookup"><span data-stu-id="bf4b7-146">Example 10: Create a context by using the OAuth Authentication</span></span>
```
C:\PS>Connect-AzureRmAccount
C:\PS> $Context = New-AzureStorageContext -StorageAccountName "myaccountname" -UseConnectedAccount
```

<span data-ttu-id="bf4b7-147">To polecenie tworzy kontekst przy użyciu uwierzytelniania OAuth.</span><span class="sxs-lookup"><span data-stu-id="bf4b7-147">This command creates a context by using the OAuth Authentication.</span></span>

## <span data-ttu-id="bf4b7-148">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bf4b7-148">PARAMETERS</span></span>

### <span data-ttu-id="bf4b7-149">-Anonymous</span><span class="sxs-lookup"><span data-stu-id="bf4b7-149">-Anonymous</span></span>
<span data-ttu-id="bf4b7-150">Wskazuje, że to polecenie cmdlet tworzy kontekst usługi Azure Storage do logowania anonimowego.</span><span class="sxs-lookup"><span data-stu-id="bf4b7-150">Indicates that this cmdlet creates an Azure Storage context for anonymous logon.</span></span>

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

### <span data-ttu-id="bf4b7-151">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="bf4b7-151">-ConnectionString</span></span>
<span data-ttu-id="bf4b7-152">Określa parametry połączenia dla kontekstu usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="bf4b7-152">Specifies a connection string for the Azure Storage context.</span></span>

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

### <span data-ttu-id="bf4b7-153">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="bf4b7-153">-Endpoint</span></span>
<span data-ttu-id="bf4b7-154">Określa punkt końcowy kontekstu usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="bf4b7-154">Specifies the endpoint for the Azure Storage context.</span></span>

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

### <span data-ttu-id="bf4b7-155">-Środowisko</span><span class="sxs-lookup"><span data-stu-id="bf4b7-155">-Environment</span></span>
<span data-ttu-id="bf4b7-156">Określa środowisko Azure.</span><span class="sxs-lookup"><span data-stu-id="bf4b7-156">Specifies the Azure environment.</span></span>
<span data-ttu-id="bf4b7-157">Dopuszczalne wartości tego parametru to: AzureCloud oraz AzureChinaCloud.</span><span class="sxs-lookup"><span data-stu-id="bf4b7-157">The acceptable values for this parameter are: AzureCloud and AzureChinaCloud.</span></span>
<span data-ttu-id="bf4b7-158">Aby uzyskać więcej informacji, wpisz tekst `Get-Help Get-AzureEnvironment` .</span><span class="sxs-lookup"><span data-stu-id="bf4b7-158">For more information, type `Get-Help Get-AzureEnvironment`.</span></span>

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

### <span data-ttu-id="bf4b7-159">-Local</span><span class="sxs-lookup"><span data-stu-id="bf4b7-159">-Local</span></span>
<span data-ttu-id="bf4b7-160">Wskazuje, że to polecenie cmdlet tworzy kontekst przy użyciu lokalnego konta magazynu dla deweloperów.</span><span class="sxs-lookup"><span data-stu-id="bf4b7-160">Indicates that this cmdlet creates a context by using the local development storage account.</span></span>

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

### <span data-ttu-id="bf4b7-161">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="bf4b7-161">-Protocol</span></span>
<span data-ttu-id="bf4b7-162">Protokół transferu (https/http).</span><span class="sxs-lookup"><span data-stu-id="bf4b7-162">Transfer Protocol (https/http).</span></span>

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

### <span data-ttu-id="bf4b7-163">-SasToken</span><span class="sxs-lookup"><span data-stu-id="bf4b7-163">-SasToken</span></span>
<span data-ttu-id="bf4b7-164">Określa token funkcji dostępu współużytkowanego (SAS, Access Signature) dla kontekstu.</span><span class="sxs-lookup"><span data-stu-id="bf4b7-164">Specifies a Shared Access Signature (SAS) token for the context.</span></span>

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

### <span data-ttu-id="bf4b7-165">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="bf4b7-165">-StorageAccountKey</span></span>
<span data-ttu-id="bf4b7-166">Określa klucz konta usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="bf4b7-166">Specifies an Azure Storage account key.</span></span>
<span data-ttu-id="bf4b7-167">To polecenie cmdlet tworzy kontekst dla klucza, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="bf4b7-167">This cmdlet creates a context for the key that this parameter specifies.</span></span>

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

### <span data-ttu-id="bf4b7-168">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="bf4b7-168">-StorageAccountName</span></span>
<span data-ttu-id="bf4b7-169">Określa nazwę konta magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="bf4b7-169">Specifies an Azure Storage account name.</span></span>
<span data-ttu-id="bf4b7-170">To polecenie cmdlet tworzy kontekst dla konta, które określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="bf4b7-170">This cmdlet creates a context for the account that this parameter specifies.</span></span>

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

### <span data-ttu-id="bf4b7-171">-UseConnectedAccount</span><span class="sxs-lookup"><span data-stu-id="bf4b7-171">-UseConnectedAccount</span></span>
<span data-ttu-id="bf4b7-172">Wskazuje, że to polecenie cmdlet tworzy kontekst usługi Azure Storage z uwierzytelnianiem uwierzytelniania OAuth.</span><span class="sxs-lookup"><span data-stu-id="bf4b7-172">Indicates that this cmdlet creates an Azure Storage context with OAuth Authentication.</span></span>
<span data-ttu-id="bf4b7-173">Polecenie cmdlet będzie domyślnie używać uwierzytelniania OAuth, jeśli nie podano innych anthentication.</span><span class="sxs-lookup"><span data-stu-id="bf4b7-173">The cmdlet will use OAuth Authentication by default, when other anthentication not specified.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: OAuthAccount, OAuthAccountEnvironment
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf4b7-174">-UseConnectedAccount</span><span class="sxs-lookup"><span data-stu-id="bf4b7-174">-UseConnectedAccount</span></span>
<span data-ttu-id="bf4b7-175">Wskazuje, że to polecenie cmdlet tworzy kontekst usługi Azure Storage z uwierzytelnianiem uwierzytelniania OAuth.</span><span class="sxs-lookup"><span data-stu-id="bf4b7-175">Indicates that this cmdlet creates an Azure Storage context with OAuth Authentication.</span></span>
<span data-ttu-id="bf4b7-176">Polecenie cmdlet będzie domyślnie używać uwierzytelniania OAuth, jeśli nie podano innych anthentication.</span><span class="sxs-lookup"><span data-stu-id="bf4b7-176">The cmdlet will use OAuth Authentication by default, when other anthentication not specified.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: OAuthAccount, OAuthAccountEnvironment
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf4b7-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf4b7-177">CommonParameters</span></span>
<span data-ttu-id="bf4b7-178">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf4b7-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf4b7-179">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf4b7-179">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf4b7-180">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bf4b7-180">INPUTS</span></span>

### <span data-ttu-id="bf4b7-181">System. String</span><span class="sxs-lookup"><span data-stu-id="bf4b7-181">System.String</span></span>

## <span data-ttu-id="bf4b7-182">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bf4b7-182">OUTPUTS</span></span>

### <span data-ttu-id="bf4b7-183">Microsoft. platformy windowsazure. Commands. Storage. AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="bf4b7-183">Microsoft.WindowsAzure.Commands.Storage.AzureStorageContext</span></span>

## <span data-ttu-id="bf4b7-184">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bf4b7-184">NOTES</span></span>

## <span data-ttu-id="bf4b7-185">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bf4b7-185">RELATED LINKS</span></span>

[<span data-ttu-id="bf4b7-186">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="bf4b7-186">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="bf4b7-187">Nowe — AzureStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="bf4b7-187">New-AzureStorageContainerSASToken</span></span>](./New-AzureStorageContainerSASToken.md)


