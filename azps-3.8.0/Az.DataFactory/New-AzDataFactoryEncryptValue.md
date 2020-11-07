---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 5BF24BC2-DEB6-4830-BDEA-841BAB070388
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactoryencryptvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryEncryptValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryEncryptValue.md
ms.openlocfilehash: 0e69cfe7ae76be1d79bdd8cf0d7db193a05219d5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93896386"
---
# <span data-ttu-id="154de-101">New-AzDataFactoryEncryptValue</span><span class="sxs-lookup"><span data-stu-id="154de-101">New-AzDataFactoryEncryptValue</span></span>

## <span data-ttu-id="154de-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="154de-102">SYNOPSIS</span></span>
<span data-ttu-id="154de-103">Szyfruje dane poufne.</span><span class="sxs-lookup"><span data-stu-id="154de-103">Encrypts sensitive data.</span></span>

## <span data-ttu-id="154de-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="154de-104">SYNTAX</span></span>

### <span data-ttu-id="154de-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="154de-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryEncryptValue [-DataFactoryName] <String> [[-Value] <SecureString>] [-GatewayName] <String>
 [[-Credential] <PSCredential>] [[-Type] <String>] [[-NonCredentialValue] <String>]
 [[-AuthenticationType] <String>] [[-Server] <String>] [[-Database] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="154de-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="154de-106">ByFactoryObject</span></span>
```
New-AzDataFactoryEncryptValue [-DataFactory] <PSDataFactory> [[-Value] <SecureString>] [-GatewayName] <String>
 [[-Credential] <PSCredential>] [[-Type] <String>] [[-NonCredentialValue] <String>]
 [[-AuthenticationType] <String>] [[-Server] <String>] [[-Database] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="154de-107">Opis</span><span class="sxs-lookup"><span data-stu-id="154de-107">DESCRIPTION</span></span>
<span data-ttu-id="154de-108">Polecenie cmdlet **New-AzDataFactoryEncryptValue** szyfruje poufne dane, takie jak hasło lub parametry połączenia z programem Microsoft SQL Server, i zwraca zaszyfrowaną wartość.</span><span class="sxs-lookup"><span data-stu-id="154de-108">The **New-AzDataFactoryEncryptValue** cmdlet encrypts sensitive data, such as a password or a Microsoft SQL Server connection string, and returns an encrypted value.</span></span>

## <span data-ttu-id="154de-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="154de-109">EXAMPLES</span></span>

### <span data-ttu-id="154de-110">Przykład 1: szyfrowanie ciągu połączenia innego niż ODBC</span><span class="sxs-lookup"><span data-stu-id="154de-110">Example 1: Encrypt a non-ODBC connection string</span></span>
```
PS C:\>$Value = ConvertTo-SecureString 'Data Source=ContosoServer;Initial Catalog=catalog;user id =user123;password=password123' -AsPlainText -Force 
PS C:\> New-AzDataFactoryEncryptValue -GatewayName "WikiGateway" -DataFactoryName "WikiAdf" -Value $value -ResourceGroupName "ADF" -Type OnPremisesSqlLinkedService
```

<span data-ttu-id="154de-111">W pierwszym poleceniu użyto polecenia cmdlet ConvertTo-SecureString, aby przekonwertować określone parametry połączenia na obiekt **SecureString** , a następnie przechowywać ten obiekt w zmiennej $Value.</span><span class="sxs-lookup"><span data-stu-id="154de-111">The first command uses the ConvertTo-SecureString cmdlet to convert the specified connection string to a **SecureString** object, and then stores that object in the $Value variable.</span></span>
<span data-ttu-id="154de-112">Aby uzyskać więcej informacji, wpisz tekst `Get-Help ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="154de-112">For more information, type `Get-Help ConvertTo-SecureString`.</span></span>
<span data-ttu-id="154de-113">Dozwolone wartości: parametry połączenia SQL Server lub Oracle.</span><span class="sxs-lookup"><span data-stu-id="154de-113">Allowed values: SQL Server or Oracle connection string.</span></span>
<span data-ttu-id="154de-114">Drugie polecenie tworzy zaszyfrowaną wartość dla obiektu przechowywanego w $Value dla określonej fabryki danych, bramy, grupy zasobów i typu połączonej usługi.</span><span class="sxs-lookup"><span data-stu-id="154de-114">The second command creates an encrypted value for the object stored in $Value for the specified data factory, gateway, resource group, and linked service type.</span></span>

### <span data-ttu-id="154de-115">Przykład 2: szyfrowanie ciągu połączenia innego niż ODBC, w którym jest używane uwierzytelnianie systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="154de-115">Example 2: Encrypt a non-ODBC connection string that uses Windows authentication.</span></span>
```
PS C:\>$Value = ConvertTo-SecureString 'Data Source=ContosoServer;Initial Catalog=catalog;Integrated Security=True' -AsPlainText -Force
PS C:\> $Credential = Get-Credential
PS C:\> New-AzDataFactoryEncryptValue -DataFactoryName "WikiADF" -GatewayName "WikiGateway" -ResourceGroupName "ADF" -Value $Value -Credential $Credential -Type OnPremisesSqlLinkedService $Value = ConvertTo-SecureString 'Data Source=ContosoServer;Initial Catalog=catalog;Integrated Security=True' -AsPlainText -Force
```

<span data-ttu-id="154de-116">W pierwszym poleceniu użyto **ConvertTo-SecureString** w celu przekonwertowania określonego ciągu połączenia na obiekt w postaci ciągu bezpiecznego, a następnie zapisanie tego obiektu w zmiennej $Value.</span><span class="sxs-lookup"><span data-stu-id="154de-116">The first command uses **ConvertTo-SecureString** to convert the specified connection string to a secure string object, and then stores that object in the $Value variable.</span></span>
<span data-ttu-id="154de-117">Drugie polecenie używa polecenia cmdlet Get-Credential w celu pobrania uwierzytelniania systemu Windows (nazwy użytkownika i hasła), a następnie zapisuje ten obiekt **PSCredential** w zmiennej $Credential.</span><span class="sxs-lookup"><span data-stu-id="154de-117">The second command uses the Get-Credential cmdlet to collect the windows authentication (user name and password), and then stores that **PSCredential** object in the $Credential variable.</span></span>
<span data-ttu-id="154de-118">Aby uzyskać więcej informacji, wpisz tekst `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="154de-118">For more information, type `Get-Help Get-Credential`.</span></span>
<span data-ttu-id="154de-119">Trzecie polecenie tworzy zaszyfrowaną wartość dla obiektu przechowywanego w $Value i $Credential dla określonej fabryki danych, bramy, grupy zasobów i typu połączonej usługi.</span><span class="sxs-lookup"><span data-stu-id="154de-119">The third command creates an encrypted value for the object stored in $Value and $Credential for the specified data factory, gateway, resource group, and linked service type.</span></span>

### <span data-ttu-id="154de-120">Przykład 3: szyfrowanie nazwy serwera i poświadczeń dla usługi połączonej z systemem plików</span><span class="sxs-lookup"><span data-stu-id="154de-120">Example 3: Encrypt server name and credentials for File system linked service</span></span>
```
PS C:\>$Value = ConvertTo-SecureString '\\servername' -AsPlainText -Force
PS C:\> $Credential = Get-Credential
PS C:\> New-AzDataFactoryEncryptValue -DataFactoryName "WikiADF" -GatewayName "WikiGateway" -ResourceGroupName "ADF" -Value $Value -Credential $Credential -Type OnPremisesFileSystemLinkedService
```

<span data-ttu-id="154de-121">W pierwszym poleceniu użyto **ConvertTo-SecureString** w celu przekonwertowania określonego ciągu na bezpieczny ciąg, a następnie zapisanie tego obiektu w zmiennej $Value.</span><span class="sxs-lookup"><span data-stu-id="154de-121">The first command uses **ConvertTo-SecureString** to convert the specified string to a secure string, and then stores that object in the $Value variable.</span></span>
<span data-ttu-id="154de-122">Drugie polecenie korzysta z **poświadczeń pobierania** w celu zebrania uwierzytelnienia systemu Windows (nazwy użytkownika i hasła), a następnie zapisuje ten obiekt **PSCredential** w zmiennej $Credential.</span><span class="sxs-lookup"><span data-stu-id="154de-122">The second command uses **Get-Credential** to collect the Windows authentication (user name and password), and then stores that **PSCredential** object in the $Credential variable.</span></span>
<span data-ttu-id="154de-123">Trzecie polecenie tworzy zaszyfrowaną wartość dla obiektu przechowywanego w $Value i $Credential dla określonej fabryki danych, bramy, grupy zasobów i typu połączonej usługi.</span><span class="sxs-lookup"><span data-stu-id="154de-123">The third command creates an encrypted value for the object stored in $Value and $Credential for the specified data factory, gateway, resource group, and linked service type.</span></span>

### <span data-ttu-id="154de-124">Przykład 4: szyfrowanie poświadczeń dla połączonej usługi HDFS</span><span class="sxs-lookup"><span data-stu-id="154de-124">Example 4: Encrypt credentials for HDFS linked service</span></span>
```
PS C:\>$UserName = ConvertTo-SecureString "domain\\username" -AsPlainText -Force
$Password = ConvertTo-SecureString "password" -AsPlainText -Force
$Credential = New-Object System.Management.Automation.PSCredential ($UserName, $Password)
New-AzDataFactoryEncryptValue -DataFactoryName "MyDataFactory" -ResourceGroupName "MyResourceGroup" -GatewayName "MyDataManagementGateway" -Type HdfsLinkedService -AuthenticationType Windows -Credential $Credential -NonCredentialValue "http://server01.com:50070/webhdfs/v1/user/username"
```

<span data-ttu-id="154de-125">Polecenie **ConvertTo-SecureString** konwertuje określony ciąg na bezpieczny ciąg.</span><span class="sxs-lookup"><span data-stu-id="154de-125">The **ConvertTo-SecureString** command converts the specified string to a secure string.</span></span>
<span data-ttu-id="154de-126">Polecenie **nowy-obiekt** tworzy obiekt PSCredential przy użyciu bezpiecznej nazwy użytkownika i ciągów haseł.</span><span class="sxs-lookup"><span data-stu-id="154de-126">The **New-Object** command creates a PSCredential object using the secure username and password strings.</span></span>
<span data-ttu-id="154de-127">Zamiast tego możesz użyć polecenia **Get-Credential** , aby zebrać uwierzytelnianie systemu Windows (nazwa użytkownika i hasło), a następnie zapisać zwrócony obiekt **PSCredential** w zmiennej $Credential, jak pokazano w poprzednich przykładach.</span><span class="sxs-lookup"><span data-stu-id="154de-127">Instead, you could use the **Get-Credential** command to collect Windows authentication (user name and password), and then store the returned **PSCredential** object in the $credential variable as shown in previous examples.</span></span>
<span data-ttu-id="154de-128">Polecenie **New-AzDataFactoryEncryptValue** tworzy zaszyfrowaną wartość dla obiektu przechowywanego w $Credential dla określonej fabryki danych, bramy, grupy zasobów i typu połączonej usługi.</span><span class="sxs-lookup"><span data-stu-id="154de-128">The **New-AzDataFactoryEncryptValue** command creates an encrypted value for the object stored in $Credential for the specified data factory, gateway, resource group, and linked service type.</span></span>

### <span data-ttu-id="154de-129">Przykład 5: szyfrowanie poświadczeń dla połączonej usługi ODBC</span><span class="sxs-lookup"><span data-stu-id="154de-129">Example 5: Encrypt credentials for ODBC linked service</span></span>
```
PS C:\>$Content = ConvertTo-SecureString "UID=username@contoso;PWD=password;" -AsPlainText -Force
New-AzDataFactoryEncryptValue -ResourceGroupName $RGName -DataFactoryName $DFName -GatewayName $Gateway -Type OnPremisesOdbcLinkedService -AuthenticationType Basic -NonCredentialValue "Driver={SQL Server};Server=server01.database.contoso.net; Database=HDISScenarioTest;" -Value $content
```

<span data-ttu-id="154de-130">Polecenie **ConvertTo-SecureString** konwertuje określony ciąg na bezpieczny ciąg.</span><span class="sxs-lookup"><span data-stu-id="154de-130">The **ConvertTo-SecureString** command converts the specified string to a secure string.</span></span>
<span data-ttu-id="154de-131">Polecenie **New-AzDataFactoryEncryptValue** tworzy zaszyfrowaną wartość dla obiektu przechowywanego w $value dla określonej fabryki danych, bramy, grupy zasobów i typu połączonej usługi.</span><span class="sxs-lookup"><span data-stu-id="154de-131">The **New-AzDataFactoryEncryptValue** command creates an encrypted value for the object stored in $Value for the specified data factory, gateway, resource group, and linked service type.</span></span>

## <span data-ttu-id="154de-132">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="154de-132">PARAMETERS</span></span>

### <span data-ttu-id="154de-133">-AuthenticationType</span><span class="sxs-lookup"><span data-stu-id="154de-133">-AuthenticationType</span></span>
<span data-ttu-id="154de-134">Określa typ uwierzytelniania, który ma być stosowany do nawiązywania połączenia ze źródłem danych.</span><span class="sxs-lookup"><span data-stu-id="154de-134">Specifies the type of authentication to be used to connect to the data source.</span></span>
<span data-ttu-id="154de-135">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="154de-135">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="154de-136">Microsoft</span><span class="sxs-lookup"><span data-stu-id="154de-136">Windows</span></span>
- <span data-ttu-id="154de-137">Podstawowym</span><span class="sxs-lookup"><span data-stu-id="154de-137">Basic</span></span>
- <span data-ttu-id="154de-138">Podłączony.</span><span class="sxs-lookup"><span data-stu-id="154de-138">Anonymous.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Windows, Basic, Anonymous

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="154de-139">— Poświadczenie</span><span class="sxs-lookup"><span data-stu-id="154de-139">-Credential</span></span>
<span data-ttu-id="154de-140">Określa poświadczenia uwierzytelniania systemu Windows (nazwa użytkownika i hasło), które mają być używane.</span><span class="sxs-lookup"><span data-stu-id="154de-140">Specifies the Windows authentication credentials (user name and password) to be used.</span></span>
<span data-ttu-id="154de-141">To polecenie cmdlet szyfruje określone tutaj dane poświadczeń.</span><span class="sxs-lookup"><span data-stu-id="154de-141">This cmdlet encrypts the credential data you specify here.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="154de-142">-Database</span><span class="sxs-lookup"><span data-stu-id="154de-142">-Database</span></span>
<span data-ttu-id="154de-143">Określa nazwę bazy danych połączonej usługi.</span><span class="sxs-lookup"><span data-stu-id="154de-143">Specifies the database name of the linked service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="154de-144">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="154de-144">-DataFactory</span></span>
<span data-ttu-id="154de-145">Określa obiekt **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="154de-145">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="154de-146">To polecenie cmdlet szyfruje dane dla fabryki danych, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="154de-146">This cmdlet encrypts data for the data factory that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="154de-147">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="154de-147">-DataFactoryName</span></span>
<span data-ttu-id="154de-148">Określa nazwę fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="154de-148">Specifies the name of a data factory.</span></span>
<span data-ttu-id="154de-149">To polecenie cmdlet szyfruje dane dla fabryki danych, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="154de-149">This cmdlet encrypts data for the data factory that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="154de-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="154de-150">-DefaultProfile</span></span>
<span data-ttu-id="154de-151">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="154de-151">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="154de-152">-Bramaname</span><span class="sxs-lookup"><span data-stu-id="154de-152">-GatewayName</span></span>
<span data-ttu-id="154de-153">Określa nazwę bramy.</span><span class="sxs-lookup"><span data-stu-id="154de-153">Specifies the name of the gateway.</span></span>
<span data-ttu-id="154de-154">To polecenie cmdlet szyfruje dane dla bramy, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="154de-154">This cmdlet encrypts data for the gateway that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="154de-155">-NonCredentialValue</span><span class="sxs-lookup"><span data-stu-id="154de-155">-NonCredentialValue</span></span>
<span data-ttu-id="154de-156">Określa część niebędącą poświadczeniem ciągu połączenia ODBC (Open Database Connectivity).</span><span class="sxs-lookup"><span data-stu-id="154de-156">Specifies the non-credential part of the Open Database Connectivity (ODBC) connection string.</span></span>
<span data-ttu-id="154de-157">Ten parametr dotyczy tylko połączonej usługi ODBC.</span><span class="sxs-lookup"><span data-stu-id="154de-157">This parameter is applicable only for the ODBC linked service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="154de-158">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="154de-158">-ResourceGroupName</span></span>
<span data-ttu-id="154de-159">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="154de-159">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="154de-160">To polecenie cmdlet szyfruje dane grupy, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="154de-160">This cmdlet encrypts data for the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="154de-161">-Server</span><span class="sxs-lookup"><span data-stu-id="154de-161">-Server</span></span>
<span data-ttu-id="154de-162">Określa nazwę serwera połączonej usługi.</span><span class="sxs-lookup"><span data-stu-id="154de-162">Specifies the server name of the linked service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="154de-163">-Type</span><span class="sxs-lookup"><span data-stu-id="154de-163">-Type</span></span>
<span data-ttu-id="154de-164">Określa typ połączonej usługi.</span><span class="sxs-lookup"><span data-stu-id="154de-164">Specifies the linked service type.</span></span>
<span data-ttu-id="154de-165">To polecenie cmdlet szyfruje dane dla typu połączonej usługi, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="154de-165">This cmdlet encrypts data for the linked service type that this parameter specifies.</span></span>
<span data-ttu-id="154de-166">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="154de-166">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="154de-167">OnPremisesSqlLinkedService</span><span class="sxs-lookup"><span data-stu-id="154de-167">OnPremisesSqlLinkedService</span></span> 
- <span data-ttu-id="154de-168">OnPremisesFileSystemLinkedService</span><span class="sxs-lookup"><span data-stu-id="154de-168">OnPremisesFileSystemLinkedService</span></span> 
- <span data-ttu-id="154de-169">OnPremisesOracleLinkedService</span><span class="sxs-lookup"><span data-stu-id="154de-169">OnPremisesOracleLinkedService</span></span> 
- <span data-ttu-id="154de-170">OnPremisesOdbcLinkedService</span><span class="sxs-lookup"><span data-stu-id="154de-170">OnPremisesOdbcLinkedService</span></span> 
- <span data-ttu-id="154de-171">OnPremisesPostgreSqlLinkedService</span><span class="sxs-lookup"><span data-stu-id="154de-171">OnPremisesPostgreSqlLinkedService</span></span> 
- <span data-ttu-id="154de-172">OnPremisesTeradataLinkedService</span><span class="sxs-lookup"><span data-stu-id="154de-172">OnPremisesTeradataLinkedService</span></span> 
- <span data-ttu-id="154de-173">OnPremisesMySQLLinkedService</span><span class="sxs-lookup"><span data-stu-id="154de-173">OnPremisesMySQLLinkedService</span></span> 
- <span data-ttu-id="154de-174">OnPremisesDB2LinkedService</span><span class="sxs-lookup"><span data-stu-id="154de-174">OnPremisesDB2LinkedService</span></span> 
- <span data-ttu-id="154de-175">OnPremisesSybaseLinkedService</span><span class="sxs-lookup"><span data-stu-id="154de-175">OnPremisesSybaseLinkedService</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: OnPremisesSqlLinkedService, OnPremisesFileSystemLinkedService, OnPremisesOracleLinkedService, OnPremisesOdbcLinkedService, OnPremisesPostgreSqlLinkedService, OnPremisesTeradataLinkedService, OnPremisesMySQLLinkedService, OnPremisesDB2LinkedService, OnPremisesSybaseLinkedService, HdfsLinkedService

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="154de-176">-Value</span><span class="sxs-lookup"><span data-stu-id="154de-176">-Value</span></span>
<span data-ttu-id="154de-177">Określa wartość do zaszyfrowania.</span><span class="sxs-lookup"><span data-stu-id="154de-177">Specifies the value to encrypt.</span></span>
<span data-ttu-id="154de-178">W przypadku lokalnej usługi SQL Server i połączonej usługi programu Oracle, użyj parametrów połączenia.</span><span class="sxs-lookup"><span data-stu-id="154de-178">For an on-premises SQL Server linked service and an on-premises Oracle linked service, use a connection string.</span></span>
<span data-ttu-id="154de-179">W przypadku lokalnej usługi połączonej ODBC Użyj części poświadczenie ciągu połączenia.</span><span class="sxs-lookup"><span data-stu-id="154de-179">For an on-premises ODBC linked service, use the credential part of the connection string.</span></span>
<span data-ttu-id="154de-180">W przypadku usługi połączonej z lokalnym systemem plików, jeśli system plików jest lokalny dla komputera bramy, Użyj lokalnego lub localhost, a jeśli system plików znajduje się na serwerze innym niż komputer bramy, użyj polecenie \\ \\ nazwa_serwera.</span><span class="sxs-lookup"><span data-stu-id="154de-180">For on premises file system linked service, if the file system is local to the gateway computer, use Local or localhost, and if the file system is on a server different from the gateway computer, use \\\\servername.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="154de-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="154de-181">CommonParameters</span></span>
<span data-ttu-id="154de-182">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="154de-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="154de-183">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="154de-183">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="154de-184">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="154de-184">INPUTS</span></span>

### <span data-ttu-id="154de-185">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="154de-185">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="154de-186">System. String</span><span class="sxs-lookup"><span data-stu-id="154de-186">System.String</span></span>

## <span data-ttu-id="154de-187">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="154de-187">OUTPUTS</span></span>

### <span data-ttu-id="154de-188">System. String</span><span class="sxs-lookup"><span data-stu-id="154de-188">System.String</span></span>

## <span data-ttu-id="154de-189">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="154de-189">NOTES</span></span>
* <span data-ttu-id="154de-190">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="154de-190">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="154de-191">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="154de-191">RELATED LINKS</span></span>

[<span data-ttu-id="154de-192">Nowe — AzDataFactoryEncryptValue</span><span class="sxs-lookup"><span data-stu-id="154de-192">New-AzDataFactoryEncryptValue</span></span>](./New-AzDataFactoryEncryptValue.md)


