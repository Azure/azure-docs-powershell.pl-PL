---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 5BF24BC2-DEB6-4830-BDEA-841BAB070388
online version: https://docs.microsoft.com/powershell/module/az.datafactory/new-azdatafactoryencryptvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryEncryptValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryEncryptValue.md
ms.openlocfilehash: 9a1f2bac984b4cad5267775dcbe59e79ed0eb677
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974977"
---
# <span data-ttu-id="a0b18-101">New-AzDataFactoryEncryptValue</span><span class="sxs-lookup"><span data-stu-id="a0b18-101">New-AzDataFactoryEncryptValue</span></span>

## <span data-ttu-id="a0b18-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0b18-102">SYNOPSIS</span></span>
<span data-ttu-id="a0b18-103">Szyfruje poufne dane.</span><span class="sxs-lookup"><span data-stu-id="a0b18-103">Encrypts sensitive data.</span></span>

## <span data-ttu-id="a0b18-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a0b18-104">SYNTAX</span></span>

### <span data-ttu-id="a0b18-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="a0b18-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryEncryptValue [-DataFactoryName] <String> [[-Value] <SecureString>] [-GatewayName] <String>
 [[-Credential] <PSCredential>] [[-Type] <String>] [[-NonCredentialValue] <String>]
 [[-AuthenticationType] <String>] [[-Server] <String>] [[-Database] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a0b18-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="a0b18-106">ByFactoryObject</span></span>
```
New-AzDataFactoryEncryptValue [-DataFactory] <PSDataFactory> [[-Value] <SecureString>] [-GatewayName] <String>
 [[-Credential] <PSCredential>] [[-Type] <String>] [[-NonCredentialValue] <String>]
 [[-AuthenticationType] <String>] [[-Server] <String>] [[-Database] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a0b18-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="a0b18-107">DESCRIPTION</span></span>
<span data-ttu-id="a0b18-108">Polecenie **cmdlet New-AzDataFactoryEncryptValue** szyfruje poufne dane, takie jak hasło lub Microsoft SQL Server połączenia, i zwraca zaszyfrowaną wartość.</span><span class="sxs-lookup"><span data-stu-id="a0b18-108">The **New-AzDataFactoryEncryptValue** cmdlet encrypts sensitive data, such as a password or a Microsoft SQL Server connection string, and returns an encrypted value.</span></span>

## <span data-ttu-id="a0b18-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a0b18-109">EXAMPLES</span></span>

### <span data-ttu-id="a0b18-110">Przykład 1. Szyfrowanie parametrów połączenia innych niż ODBC</span><span class="sxs-lookup"><span data-stu-id="a0b18-110">Example 1: Encrypt a non-ODBC connection string</span></span>
```
PS C:\>$Value = ConvertTo-SecureString 'Data Source=ContosoServer;Initial Catalog=catalog;user id =user123;password=password123' -AsPlainText -Force 
PS C:\> New-AzDataFactoryEncryptValue -GatewayName "WikiGateway" -DataFactoryName "WikiAdf" -Value $value -ResourceGroupName "ADF" -Type OnPremisesSqlLinkedService
```

<span data-ttu-id="a0b18-111">Pierwsze polecenie używa ConvertTo-SecureString cmdlet w celu przekonwertowania określonych parametrów połączenia na obiekt **SecureString,** a następnie zapisuje ten obiekt w $Value danych.</span><span class="sxs-lookup"><span data-stu-id="a0b18-111">The first command uses the ConvertTo-SecureString cmdlet to convert the specified connection string to a **SecureString** object, and then stores that object in the $Value variable.</span></span>
<span data-ttu-id="a0b18-112">Aby uzyskać więcej informacji, wpisz `Get-Help ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="a0b18-112">For more information, type `Get-Help ConvertTo-SecureString`.</span></span>
<span data-ttu-id="a0b18-113">Dozwolone wartości: ciąg połączenia programu SQL Server lub Oracle.</span><span class="sxs-lookup"><span data-stu-id="a0b18-113">Allowed values: SQL Server or Oracle connection string.</span></span>
<span data-ttu-id="a0b18-114">Drugie polecenie tworzy zaszyfrowaną wartość obiektu przechowywanego w usłudze $Value dla określonej fabrycznej, bramy, grupy zasobów i połączonego typu usługi.</span><span class="sxs-lookup"><span data-stu-id="a0b18-114">The second command creates an encrypted value for the object stored in $Value for the specified data factory, gateway, resource group, and linked service type.</span></span>

### <span data-ttu-id="a0b18-115">Przykład 2. Szyfrowanie parametrów połączenia innych niż ODBC, które używa uwierzytelniania systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="a0b18-115">Example 2: Encrypt a non-ODBC connection string that uses Windows authentication.</span></span>
```
PS C:\>$Value = ConvertTo-SecureString 'Data Source=ContosoServer;Initial Catalog=catalog;Integrated Security=True' -AsPlainText -Force
PS C:\> $Credential = Get-Credential
PS C:\> New-AzDataFactoryEncryptValue -DataFactoryName "WikiADF" -GatewayName "WikiGateway" -ResourceGroupName "ADF" -Value $Value -Credential $Credential -Type OnPremisesSqlLinkedService $Value = ConvertTo-SecureString 'Data Source=ContosoServer;Initial Catalog=catalog;Integrated Security=True' -AsPlainText -Force
```

<span data-ttu-id="a0b18-116">Pierwsze polecenie używa **formatu ConvertTo-SecureString** w celu przekonwertowania określonych parametrów połączenia na bezpieczny obiekt ciągu, a następnie zapisuje ten obiekt w $Value danych.</span><span class="sxs-lookup"><span data-stu-id="a0b18-116">The first command uses **ConvertTo-SecureString** to convert the specified connection string to a secure string object, and then stores that object in the $Value variable.</span></span>
<span data-ttu-id="a0b18-117">Drugie polecenie używa polecenia cmdlet Get-Credential do zbierania uwierzytelniania systemu Windows (nazwy użytkownika i hasła), a następnie zapisuje ten obiekt **PSCredential** w $Credential danych.</span><span class="sxs-lookup"><span data-stu-id="a0b18-117">The second command uses the Get-Credential cmdlet to collect the windows authentication (user name and password), and then stores that **PSCredential** object in the $Credential variable.</span></span>
<span data-ttu-id="a0b18-118">Aby uzyskać więcej informacji, wpisz `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="a0b18-118">For more information, type `Get-Help Get-Credential`.</span></span>
<span data-ttu-id="a0b18-119">Trzecie polecenie tworzy zaszyfrowaną wartość obiektu przechowywanego w usłudze $Value i $Credential dla określonej fabrycznej, bramy, grupy zasobów i połączonego typu usługi.</span><span class="sxs-lookup"><span data-stu-id="a0b18-119">The third command creates an encrypted value for the object stored in $Value and $Credential for the specified data factory, gateway, resource group, and linked service type.</span></span>

### <span data-ttu-id="a0b18-120">Przykład 3. Szyfrowanie nazwy serwera i poświadczeń dla połączonej usługi systemu plików</span><span class="sxs-lookup"><span data-stu-id="a0b18-120">Example 3: Encrypt server name and credentials for File system linked service</span></span>
```
PS C:\>$Value = ConvertTo-SecureString '\\servername' -AsPlainText -Force
PS C:\> $Credential = Get-Credential
PS C:\> New-AzDataFactoryEncryptValue -DataFactoryName "WikiADF" -GatewayName "WikiGateway" -ResourceGroupName "ADF" -Value $Value -Credential $Credential -Type OnPremisesFileSystemLinkedService
```

<span data-ttu-id="a0b18-121">Pierwsze polecenie konwertuje określony ciąg na bezpieczny ciąg za pomocą ciągu **ConvertTo-SecureString,** a następnie zapisuje ten obiekt w $Value danych.</span><span class="sxs-lookup"><span data-stu-id="a0b18-121">The first command uses **ConvertTo-SecureString** to convert the specified string to a secure string, and then stores that object in the $Value variable.</span></span>
<span data-ttu-id="a0b18-122">Drugie polecenie używa polecenia **Get-Credential** do zbierania uwierzytelniania systemu Windows (nazwy użytkownika i hasła), a następnie zapisuje ten obiekt **PSCredential** w $Credential danych.</span><span class="sxs-lookup"><span data-stu-id="a0b18-122">The second command uses **Get-Credential** to collect the Windows authentication (user name and password), and then stores that **PSCredential** object in the $Credential variable.</span></span>
<span data-ttu-id="a0b18-123">Trzecie polecenie tworzy zaszyfrowaną wartość obiektu przechowywanego w usłudze $Value i $Credential dla określonej fabrycznej, bramy, grupy zasobów i połączonego typu usługi.</span><span class="sxs-lookup"><span data-stu-id="a0b18-123">The third command creates an encrypted value for the object stored in $Value and $Credential for the specified data factory, gateway, resource group, and linked service type.</span></span>

### <span data-ttu-id="a0b18-124">Przykład 4. Szyfrowanie poświadczeń dla usługi połączonej HDFS</span><span class="sxs-lookup"><span data-stu-id="a0b18-124">Example 4: Encrypt credentials for HDFS linked service</span></span>
```
PS C:\>$UserName = ConvertTo-SecureString "domain\\username" -AsPlainText -Force
$Password = ConvertTo-SecureString "password" -AsPlainText -Force
$Credential = New-Object System.Management.Automation.PSCredential ($UserName, $Password)
New-AzDataFactoryEncryptValue -DataFactoryName "MyDataFactory" -ResourceGroupName "MyResourceGroup" -GatewayName "MyDataManagementGateway" -Type HdfsLinkedService -AuthenticationType Windows -Credential $Credential -NonCredentialValue "http://server01.com:50070/webhdfs/v1/user/username"
```

<span data-ttu-id="a0b18-125">Polecenie **ConvertTo-SecureString** konwertuje określony ciąg na bezpieczny ciąg.</span><span class="sxs-lookup"><span data-stu-id="a0b18-125">The **ConvertTo-SecureString** command converts the specified string to a secure string.</span></span>
<span data-ttu-id="a0b18-126">Polecenie **Nowy obiekt tworzy** obiekt PSCredential przy użyciu ciągów bezpiecznej nazwy użytkownika i hasła.</span><span class="sxs-lookup"><span data-stu-id="a0b18-126">The **New-Object** command creates a PSCredential object using the secure username and password strings.</span></span>
<span data-ttu-id="a0b18-127">Zamiast tego można użyć polecenia **Get-Credential** w celu zebrania uwierzytelniania systemu Windows (nazwy użytkownika i hasła), a następnie przechowywać zwrócony obiekt **PSCredential** w zmiennej $credential, jak pokazano w poprzednich przykładach.</span><span class="sxs-lookup"><span data-stu-id="a0b18-127">Instead, you could use the **Get-Credential** command to collect Windows authentication (user name and password), and then store the returned **PSCredential** object in the $credential variable as shown in previous examples.</span></span>
<span data-ttu-id="a0b18-128">Polecenie **New-AzDataFactoryEncryptValue** tworzy zaszyfrowaną wartość obiektu przechowywanego w usłudze $Credential dla określonego typu usługi, bramy, grupy zasobów i połączonej usługi.</span><span class="sxs-lookup"><span data-stu-id="a0b18-128">The **New-AzDataFactoryEncryptValue** command creates an encrypted value for the object stored in $Credential for the specified data factory, gateway, resource group, and linked service type.</span></span>

### <span data-ttu-id="a0b18-129">Przykład 5. Szyfrowanie poświadczeń dla usługi połączonej ODBC</span><span class="sxs-lookup"><span data-stu-id="a0b18-129">Example 5: Encrypt credentials for ODBC linked service</span></span>
```
PS C:\>$Content = ConvertTo-SecureString "UID=username@contoso;PWD=password;" -AsPlainText -Force
New-AzDataFactoryEncryptValue -ResourceGroupName $RGName -DataFactoryName $DFName -GatewayName $Gateway -Type OnPremisesOdbcLinkedService -AuthenticationType Basic -NonCredentialValue "Driver={SQL Server};Server=server01.database.contoso.net; Database=HDISScenarioTest;" -Value $content
```

<span data-ttu-id="a0b18-130">Polecenie **ConvertTo-SecureString** konwertuje określony ciąg na bezpieczny ciąg.</span><span class="sxs-lookup"><span data-stu-id="a0b18-130">The **ConvertTo-SecureString** command converts the specified string to a secure string.</span></span>
<span data-ttu-id="a0b18-131">Polecenie **New-AzDataFactoryEncryptValue** tworzy zaszyfrowaną wartość obiektu przechowywanego w usłudze $Value dla określonego typu usługi, bramy, grupy zasobów i połączonego typu usługi.</span><span class="sxs-lookup"><span data-stu-id="a0b18-131">The **New-AzDataFactoryEncryptValue** command creates an encrypted value for the object stored in $Value for the specified data factory, gateway, resource group, and linked service type.</span></span>

## <span data-ttu-id="a0b18-132">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a0b18-132">PARAMETERS</span></span>

### <span data-ttu-id="a0b18-133">-AuthenticationType</span><span class="sxs-lookup"><span data-stu-id="a0b18-133">-AuthenticationType</span></span>
<span data-ttu-id="a0b18-134">Określa typ uwierzytelniania używanego do łączenia się ze źródłem danych.</span><span class="sxs-lookup"><span data-stu-id="a0b18-134">Specifies the type of authentication to be used to connect to the data source.</span></span>
<span data-ttu-id="a0b18-135">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="a0b18-135">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a0b18-136">Windows</span><span class="sxs-lookup"><span data-stu-id="a0b18-136">Windows</span></span>
- <span data-ttu-id="a0b18-137">Podstawowe</span><span class="sxs-lookup"><span data-stu-id="a0b18-137">Basic</span></span>
- <span data-ttu-id="a0b18-138">Anonimowe.</span><span class="sxs-lookup"><span data-stu-id="a0b18-138">Anonymous.</span></span>

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

### <span data-ttu-id="a0b18-139">- Credential</span><span class="sxs-lookup"><span data-stu-id="a0b18-139">-Credential</span></span>
<span data-ttu-id="a0b18-140">Określa używane poświadczenia uwierzytelniania systemu Windows (nazwę użytkownika i hasło).</span><span class="sxs-lookup"><span data-stu-id="a0b18-140">Specifies the Windows authentication credentials (user name and password) to be used.</span></span>
<span data-ttu-id="a0b18-141">To polecenie cmdlet szyfruje określone tutaj dane poświadczeń.</span><span class="sxs-lookup"><span data-stu-id="a0b18-141">This cmdlet encrypts the credential data you specify here.</span></span>

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

### <span data-ttu-id="a0b18-142">— Baza danych</span><span class="sxs-lookup"><span data-stu-id="a0b18-142">-Database</span></span>
<span data-ttu-id="a0b18-143">Określa nazwę bazy danych usługi połączonej.</span><span class="sxs-lookup"><span data-stu-id="a0b18-143">Specifies the database name of the linked service.</span></span>

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

### <span data-ttu-id="a0b18-144">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="a0b18-144">-DataFactory</span></span>
<span data-ttu-id="a0b18-145">Określa obiekt **PSDataFactory.**</span><span class="sxs-lookup"><span data-stu-id="a0b18-145">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="a0b18-146">To polecenie cmdlet szyfruje dane dla fabrycznych danych określanych przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="a0b18-146">This cmdlet encrypts data for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="a0b18-147">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="a0b18-147">-DataFactoryName</span></span>
<span data-ttu-id="a0b18-148">Określa nazwę fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="a0b18-148">Specifies the name of a data factory.</span></span>
<span data-ttu-id="a0b18-149">To polecenie cmdlet szyfruje dane dla fabrycznych danych określanych przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="a0b18-149">This cmdlet encrypts data for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="a0b18-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0b18-150">-DefaultProfile</span></span>
<span data-ttu-id="a0b18-151">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="a0b18-151">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a0b18-152">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="a0b18-152">-GatewayName</span></span>
<span data-ttu-id="a0b18-153">Określa nazwę bramy.</span><span class="sxs-lookup"><span data-stu-id="a0b18-153">Specifies the name of the gateway.</span></span>
<span data-ttu-id="a0b18-154">To polecenie cmdlet szyfruje dane bramy, które określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="a0b18-154">This cmdlet encrypts data for the gateway that this parameter specifies.</span></span>

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

### <span data-ttu-id="a0b18-155">-NonCredentialValue</span><span class="sxs-lookup"><span data-stu-id="a0b18-155">-NonCredentialValue</span></span>
<span data-ttu-id="a0b18-156">Określa część połączenia ODBC (Open Database Connectivity) bez poświadczeń.</span><span class="sxs-lookup"><span data-stu-id="a0b18-156">Specifies the non-credential part of the Open Database Connectivity (ODBC) connection string.</span></span>
<span data-ttu-id="a0b18-157">Ten parametr ma zastosowanie tylko do usługi połączonej ODBC.</span><span class="sxs-lookup"><span data-stu-id="a0b18-157">This parameter is applicable only for the ODBC linked service.</span></span>

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

### <span data-ttu-id="a0b18-158">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0b18-158">-ResourceGroupName</span></span>
<span data-ttu-id="a0b18-159">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a0b18-159">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="a0b18-160">To polecenie cmdlet szyfruje dane dla grupy, która określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="a0b18-160">This cmdlet encrypts data for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="a0b18-161">— Serwer</span><span class="sxs-lookup"><span data-stu-id="a0b18-161">-Server</span></span>
<span data-ttu-id="a0b18-162">Określa nazwę serwera połączonej usługi.</span><span class="sxs-lookup"><span data-stu-id="a0b18-162">Specifies the server name of the linked service.</span></span>

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

### <span data-ttu-id="a0b18-163">— Wpisz</span><span class="sxs-lookup"><span data-stu-id="a0b18-163">-Type</span></span>
<span data-ttu-id="a0b18-164">Określa typ połączonej usługi.</span><span class="sxs-lookup"><span data-stu-id="a0b18-164">Specifies the linked service type.</span></span>
<span data-ttu-id="a0b18-165">To polecenie cmdlet szyfruje dane dla połączonego typu usługi, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="a0b18-165">This cmdlet encrypts data for the linked service type that this parameter specifies.</span></span>
<span data-ttu-id="a0b18-166">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="a0b18-166">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a0b18-167">OnPremisesSqlLinkedService</span><span class="sxs-lookup"><span data-stu-id="a0b18-167">OnPremisesSqlLinkedService</span></span> 
- <span data-ttu-id="a0b18-168">OnPremisesFileSystemLinkedService</span><span class="sxs-lookup"><span data-stu-id="a0b18-168">OnPremisesFileSystemLinkedService</span></span> 
- <span data-ttu-id="a0b18-169">OnPremisesOracleLinkedService</span><span class="sxs-lookup"><span data-stu-id="a0b18-169">OnPremisesOracleLinkedService</span></span> 
- <span data-ttu-id="a0b18-170">OnPremisesOdbcLinkedService</span><span class="sxs-lookup"><span data-stu-id="a0b18-170">OnPremisesOdbcLinkedService</span></span> 
- <span data-ttu-id="a0b18-171">OnPremisesPostgreSqlLinkedService</span><span class="sxs-lookup"><span data-stu-id="a0b18-171">OnPremisesPostgreSqlLinkedService</span></span> 
- <span data-ttu-id="a0b18-172">OnPremisesTeradataLinkedService</span><span class="sxs-lookup"><span data-stu-id="a0b18-172">OnPremisesTeradataLinkedService</span></span> 
- <span data-ttu-id="a0b18-173">OnPremisesMySQLLinkedService</span><span class="sxs-lookup"><span data-stu-id="a0b18-173">OnPremisesMySQLLinkedService</span></span> 
- <span data-ttu-id="a0b18-174">OnPremisesDB2LinkedService</span><span class="sxs-lookup"><span data-stu-id="a0b18-174">OnPremisesDB2LinkedService</span></span> 
- <span data-ttu-id="a0b18-175">OnPremisesSybaseLinkedService</span><span class="sxs-lookup"><span data-stu-id="a0b18-175">OnPremisesSybaseLinkedService</span></span>

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

### <span data-ttu-id="a0b18-176">— Wartość</span><span class="sxs-lookup"><span data-stu-id="a0b18-176">-Value</span></span>
<span data-ttu-id="a0b18-177">Określa wartość do zaszyfrowania.</span><span class="sxs-lookup"><span data-stu-id="a0b18-177">Specifies the value to encrypt.</span></span>
<span data-ttu-id="a0b18-178">W przypadku lokalnej usługi połączonej programu SQL Server i lokalnej usługi połączonej Oracle użyj parametrów połączenia.</span><span class="sxs-lookup"><span data-stu-id="a0b18-178">For an on-premises SQL Server linked service and an on-premises Oracle linked service, use a connection string.</span></span>
<span data-ttu-id="a0b18-179">W przypadku lokalnej usługi połączonej ODBC należy użyć części poświadczeń parametrów połączenia.</span><span class="sxs-lookup"><span data-stu-id="a0b18-179">For an on-premises ODBC linked service, use the credential part of the connection string.</span></span>
<span data-ttu-id="a0b18-180">W przypadku usługi połączonej w lokalnym systemie plików, jeśli system plików jest lokalny na komputerze bramy, użyj wartości Local lub localhost, a jeśli system plików znajduje się na serwerze innym niż komputer bramy, użyj nazwy \\ \\ serwera.</span><span class="sxs-lookup"><span data-stu-id="a0b18-180">For on premises file system linked service, if the file system is local to the gateway computer, use Local or localhost, and if the file system is on a server different from the gateway computer, use \\\\servername.</span></span>

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

### <span data-ttu-id="a0b18-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0b18-181">CommonParameters</span></span>
<span data-ttu-id="a0b18-182">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0b18-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0b18-183">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0b18-183">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0b18-184">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a0b18-184">INPUTS</span></span>

### <span data-ttu-id="a0b18-185">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="a0b18-185">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="a0b18-186">System.String</span><span class="sxs-lookup"><span data-stu-id="a0b18-186">System.String</span></span>

## <span data-ttu-id="a0b18-187">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a0b18-187">OUTPUTS</span></span>

### <span data-ttu-id="a0b18-188">System.String</span><span class="sxs-lookup"><span data-stu-id="a0b18-188">System.String</span></span>

## <span data-ttu-id="a0b18-189">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a0b18-189">NOTES</span></span>
* <span data-ttu-id="a0b18-190">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="a0b18-190">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="a0b18-191">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a0b18-191">RELATED LINKS</span></span>

[<span data-ttu-id="a0b18-192">New-AzDataFactoryEncryptValue</span><span class="sxs-lookup"><span data-stu-id="a0b18-192">New-AzDataFactoryEncryptValue</span></span>](./New-AzDataFactoryEncryptValue.md)


