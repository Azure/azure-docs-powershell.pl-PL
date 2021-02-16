---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: B7B29875-D2E5-4E96-AD4B-83032AB18D02
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5312556cb49d02ea901b4cb2526a36f7237f66d1
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100404177"
---
# <span data-ttu-id="b5fbe-101">New-AzureSqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="b5fbe-101">New-AzureSqlDatabaseServerContext</span></span>

## <span data-ttu-id="b5fbe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5fbe-102">SYNOPSIS</span></span>
<span data-ttu-id="b5fbe-103">Tworzy kontekst połączenia z serwerem.</span><span class="sxs-lookup"><span data-stu-id="b5fbe-103">Creates a server connection context.</span></span>

## <span data-ttu-id="b5fbe-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b5fbe-104">SYNTAX</span></span>

### <span data-ttu-id="b5fbe-105">ByServerNameWithSqlAuth (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="b5fbe-105">ByServerNameWithSqlAuth (Default)</span></span>
```
New-AzureSqlDatabaseServerContext -ServerName <String> -Credential <PSCredential> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="b5fbe-106">ByManageUrlWithSqlAuth</span><span class="sxs-lookup"><span data-stu-id="b5fbe-106">ByManageUrlWithSqlAuth</span></span>
```
New-AzureSqlDatabaseServerContext [-ServerName <String>] -ManageUrl <Uri> -Credential <PSCredential>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="b5fbe-107">ByServerNameWithCertAuth</span><span class="sxs-lookup"><span data-stu-id="b5fbe-107">ByServerNameWithCertAuth</span></span>
```
New-AzureSqlDatabaseServerContext -ServerName <String> [-UseSubscription] [-SubscriptionName <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="b5fbe-108">ByFullyQualifiedServerNameWithSqlAuth</span><span class="sxs-lookup"><span data-stu-id="b5fbe-108">ByFullyQualifiedServerNameWithSqlAuth</span></span>
```
New-AzureSqlDatabaseServerContext -FullyQualifiedServerName <String> -Credential <PSCredential>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="b5fbe-109">ByFullyQualifiedServerNameWithCertAuth</span><span class="sxs-lookup"><span data-stu-id="b5fbe-109">ByFullyQualifiedServerNameWithCertAuth</span></span>
```
New-AzureSqlDatabaseServerContext -FullyQualifiedServerName <String> [-UseSubscription]
 [-SubscriptionName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b5fbe-110">OPIS</span><span class="sxs-lookup"><span data-stu-id="b5fbe-110">DESCRIPTION</span></span>
<span data-ttu-id="b5fbe-111">Polecenie **cmdlet New-AzureSqlDatabaseServerContext** tworzy kontekst połączenia z serwerem usługi Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="b5fbe-111">The **New-AzureSqlDatabaseServerContext** cmdlet creates an Azure SQL Database server connection context.</span></span>
<span data-ttu-id="b5fbe-112">Uwierzytelnianie programu SQL Server umożliwia utworzenie kontekstu połączenia z serwerem bazy danych SQL przy użyciu określonych poświadczeń.</span><span class="sxs-lookup"><span data-stu-id="b5fbe-112">Use SQL Server authentication to create a connection context to a SQL Database server by using the specified credentials.</span></span>
<span data-ttu-id="b5fbe-113">Serwer bazy danych SQL można określić według nazwy, w pełni kwalifikowanej nazwy lub adresu URL.</span><span class="sxs-lookup"><span data-stu-id="b5fbe-113">You can specify the SQL Database server by name, by the fully qualified name, or by URL.</span></span>
<span data-ttu-id="b5fbe-114">Aby uzyskać poświadczenia, użyj polecenia cmdlet Get-Credential monit o podanie nazwy użytkownika i hasła.</span><span class="sxs-lookup"><span data-stu-id="b5fbe-114">To obtain a credential, use the Get-Credential cmdlet that prompts you to specify the user name and password.</span></span>

<span data-ttu-id="b5fbe-115">Użyj polecenia cmdlet **New-AzureSqlDatabaseServerContext** z uwierzytelnianiem opartym na certyfikatach, aby utworzyć kontekst połączenia z określonym serwerem bazy danych SQL przy użyciu określonych danych subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b5fbe-115">Use the **New-AzureSqlDatabaseServerContext** cmdlet with certificate based authentication to create a connection context to the specified SQL Database server by using the specified Azure subscription data.</span></span>
<span data-ttu-id="b5fbe-116">Serwer bazy danych SQL można określić według nazwy lub w pełni kwalifikowanej nazwy.</span><span class="sxs-lookup"><span data-stu-id="b5fbe-116">You can specify SQL Database server by name or by the fully qualified name.</span></span>
<span data-ttu-id="b5fbe-117">Możesz określić dane subskrypcji jako parametr lub pobrać je z bieżącej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b5fbe-117">You can specify the subscription data as a parameter or it can be retrieved from the current Azure subscription.</span></span>
<span data-ttu-id="b5fbe-118">Użyj polecenia cmdlet Select-AzureSubscription, https://msdn.microsoft.com/library/windowsazure/jj152833.aspx aby wybrać bieżącą subskrypcję platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b5fbe-118">Use the Select-AzureSubscriptionhttps://msdn.microsoft.com/library/windowsazure/jj152833.aspx cmdlet to select the current Azure subscription.</span></span>

## <span data-ttu-id="b5fbe-119">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b5fbe-119">EXAMPLES</span></span>

### <span data-ttu-id="b5fbe-120">Przykład 1. Tworzenie kontekstu przy użyciu uwierzytelniania programu SQL Server</span><span class="sxs-lookup"><span data-stu-id="b5fbe-120">Example 1: Create a context by using SQL Server authentication</span></span>
```
PS C:\> $Credential = Get-Credential
PS C:\> $Context = New-AzureSqlDatabaseServerContext -ServerName "lpqd0zbr8y" -Credential $Credential
PS C:\> $Database17 = New-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database17" -MaxSizeGB 50 -Collation "SQL_Latin1_General_CP1_CI_AS"
```

<span data-ttu-id="b5fbe-121">W tym przykładzie użyto uwierzytelniania programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b5fbe-121">This example uses the SQL Server authentication.</span></span>

<span data-ttu-id="b5fbe-122">Pierwsze polecenie monituje o poświadczenia administratora serwera i zapisuje poświadczenia w $Credential danych.</span><span class="sxs-lookup"><span data-stu-id="b5fbe-122">The first command prompts you for server administrator credentials, and stores the credentials in the $Credential variable.</span></span>

<span data-ttu-id="b5fbe-123">Drugie polecenie łączy się z serwerem bazy danych SQL o nazwie lpqd0zbr8y przy użyciu $Credential.</span><span class="sxs-lookup"><span data-stu-id="b5fbe-123">The second command connects to the SQL Database server named lpqd0zbr8y by using $Credential.</span></span>

<span data-ttu-id="b5fbe-124">Ostatnie polecenie tworzy na serwerze bazę danych o nazwie Database17, która stanowi część kontekstu w $Context.</span><span class="sxs-lookup"><span data-stu-id="b5fbe-124">The final command creates a database named Database17 on the server that is part of the context in $Context.</span></span>

### <span data-ttu-id="b5fbe-125">Przykład 2. Tworzenie kontekstu przy użyciu uwierzytelniania na podstawie certyfikatu</span><span class="sxs-lookup"><span data-stu-id="b5fbe-125">Example 2: Create a context by using certificate based authentication</span></span>
```
PS C:\> $SubscriptionId = <Subscription ID>
PS C:\> $Thumbprint = <Certificate Thumbprint>
PS C:\> $Certificate = Get-Item "Cert:\CurrentUser\My\$Thumbprint"
PS C:\> Set-AzureSubscription -SubscriptionName "Subscription07" -SubscriptionId $SubscriptionId -Certificate $Certificate
PS C:\> Select-AzureSubscription -SubscriptionName "Subscription07"
PS C:\> $Context = New-AzureSqlDatabaseServerContext -ServerName "lpqd0zbr8y" -UseSubscription
```

<span data-ttu-id="b5fbe-126">W tym przykładzie jest używane uwierzytelnianie na podstawie certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="b5fbe-126">This example uses the certificate based authentication.</span></span>

<span data-ttu-id="b5fbe-127">Pierwsze dwa polecenia przypiszą wartości do zmiennych $SubscriptionId i $Thumbprint zmiennych.</span><span class="sxs-lookup"><span data-stu-id="b5fbe-127">The first two commands assign values to the $SubscriptionId and $Thumbprint variables.</span></span>

<span data-ttu-id="b5fbe-128">Trzecie polecenie pobiera certyfikat oznaczony kciukiem w programie $Thumbprint i przechowuje go w $Certificate.</span><span class="sxs-lookup"><span data-stu-id="b5fbe-128">The third command gets the certificate identified by the thumbprint in $Thumbprint, and stores it in $Certificate.</span></span>

<span data-ttu-id="b5fbe-129">Czwarte polecenie ustawia subskrypcję jako subskrypcję 07, a piąte polecenie wybiera tę subskrypcję.</span><span class="sxs-lookup"><span data-stu-id="b5fbe-129">The fourth command sets the subscription to be Subscription07, and the fifth command selects that subscription.</span></span>

<span data-ttu-id="b5fbe-130">Ostatnie polecenie tworzy kontekst w bieżącej subskrypcji dla serwera o nazwie lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="b5fbe-130">The final command creates a context in the current subscription for the server named lpqd0zbr8y.</span></span>

## <span data-ttu-id="b5fbe-131">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b5fbe-131">PARAMETERS</span></span>

### <span data-ttu-id="b5fbe-132">- Credential</span><span class="sxs-lookup"><span data-stu-id="b5fbe-132">-Credential</span></span>
<span data-ttu-id="b5fbe-133">Określa obiekt poświadczeń, który zapewnia uwierzytelnianie programu SQL Server w celu uzyskania dostępu do serwera.</span><span class="sxs-lookup"><span data-stu-id="b5fbe-133">Specifies a credential object that provides SQL Server authentication for you to access the server.</span></span>

```yaml
Type: PSCredential
Parameter Sets: ByServerNameWithSqlAuth, ByManageUrlWithSqlAuth, ByFullyQualifiedServerNameWithSqlAuth
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5fbe-134">-FullyQualifiedServerName</span><span class="sxs-lookup"><span data-stu-id="b5fbe-134">-FullyQualifiedServerName</span></span>
<span data-ttu-id="b5fbe-135">Określa w pełni kwalifikowaną nazwę domeny (FQDN) dla serwera usługi Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="b5fbe-135">Specifies the fully qualified domain name (FQDN) name for the Azure SQL Database server.</span></span>
<span data-ttu-id="b5fbe-136">Na przykład Server02.database.windows.net.</span><span class="sxs-lookup"><span data-stu-id="b5fbe-136">For example, Server02.database.windows.net.</span></span>

```yaml
Type: String
Parameter Sets: ByFullyQualifiedServerNameWithSqlAuth, ByFullyQualifiedServerNameWithCertAuth
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5fbe-137">- ManageUrl</span><span class="sxs-lookup"><span data-stu-id="b5fbe-137">-ManageUrl</span></span>
<span data-ttu-id="b5fbe-138">Określa adres URL używany przez to polecenie cmdlet do uzyskiwania dostępu do portalu Azure SQL DatabaseManagement dla serwera.</span><span class="sxs-lookup"><span data-stu-id="b5fbe-138">Specifies the URL that this cmdlet uses to access the Azure SQL DatabaseManagement Portal for the server.</span></span>

```yaml
Type: Uri
Parameter Sets: ByManageUrlWithSqlAuth
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5fbe-139">— Profil</span><span class="sxs-lookup"><span data-stu-id="b5fbe-139">-Profile</span></span>
<span data-ttu-id="b5fbe-140">Określa profil platformy Azure, z którego będzie odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5fbe-140">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b5fbe-141">Jeśli nie określisz profilu, to polecenie cmdlet zostanie odczytane z lokalnego profilu domyślnego.</span><span class="sxs-lookup"><span data-stu-id="b5fbe-141">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5fbe-142">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b5fbe-142">-ServerName</span></span>
<span data-ttu-id="b5fbe-143">Określa nazwę serwera bazy danych.</span><span class="sxs-lookup"><span data-stu-id="b5fbe-143">Specifies the name of the database server.</span></span>

```yaml
Type: String
Parameter Sets: ByServerNameWithSqlAuth, ByServerNameWithCertAuth
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByManageUrlWithSqlAuth
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5fbe-144">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="b5fbe-144">-SubscriptionName</span></span>
<span data-ttu-id="b5fbe-145">Określa nazwę subskrypcji platformy Azure, za pomocą których to polecenie cmdlet tworzy kontekst połączenia.</span><span class="sxs-lookup"><span data-stu-id="b5fbe-145">Specifies the name of the Azure subscription that this cmdlet uses to create the connection context.</span></span>
<span data-ttu-id="b5fbe-146">Jeśli nie określisz wartości dla tego parametru, polecenie cmdlet użyje bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="b5fbe-146">If you do not specify a value for this parameter, the cmdlet uses the current subscription.</span></span>
<span data-ttu-id="b5fbe-147">Uruchom Select-AzureSubscription cmdlet, aby zmienić bieżącą subskrypcję.</span><span class="sxs-lookup"><span data-stu-id="b5fbe-147">Run the Select-AzureSubscription cmdlet to change the current subscription.</span></span>

```yaml
Type: String
Parameter Sets: ByServerNameWithCertAuth, ByFullyQualifiedServerNameWithCertAuth
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5fbe-148">—UseSubscription</span><span class="sxs-lookup"><span data-stu-id="b5fbe-148">-UseSubscription</span></span>
<span data-ttu-id="b5fbe-149">Wskazuje, że to polecenie cmdlet tworzy kontekst połączenia za pomocą subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b5fbe-149">Indicates that this cmdlet uses Azure subscription for creating the connection context.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByServerNameWithCertAuth, ByFullyQualifiedServerNameWithCertAuth
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5fbe-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5fbe-150">CommonParameters</span></span>
<span data-ttu-id="b5fbe-151">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5fbe-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5fbe-152">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5fbe-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5fbe-153">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b5fbe-153">INPUTS</span></span>

## <span data-ttu-id="b5fbe-154">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b5fbe-154">OUTPUTS</span></span>

### <span data-ttu-id="b5fbe-155">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.IServerDataServiceContext</span><span class="sxs-lookup"><span data-stu-id="b5fbe-155">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.IServerDataServiceContext</span></span>

## <span data-ttu-id="b5fbe-156">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b5fbe-156">NOTES</span></span>
* <span data-ttu-id="b5fbe-157">Jeśli uwierzytelnianie nie określa domeny, a w przypadku korzystania z programu Windows PowerShell 2.0 polecenie cmdlet Get-Credential zwraca ukośnik odwrotny () przed nazwą użytkownika, na przykład \\ \user.</span><span class="sxs-lookup"><span data-stu-id="b5fbe-157">If you authenticate without specifying a domain, and if you use Windows PowerShell 2.0, the Get-Credential cmdlet returns a backslash (\\) prepended to the username, for example, \user.</span></span> <span data-ttu-id="b5fbe-158">Program Windows PowerShell 3.0 nie dodaje ukośnika odwrotnego.</span><span class="sxs-lookup"><span data-stu-id="b5fbe-158">Windows PowerShell 3.0 does not add the backslash.</span></span> <span data-ttu-id="b5fbe-159">Ten ukośnik odwrotny nie jest rozpoznawany przez parametr *Credential* polecenia cmdlet **New-AzureSqlDatabaseServerContext.**</span><span class="sxs-lookup"><span data-stu-id="b5fbe-159">This backslash is not recognized by the *Credential* parameter of the **New-AzureSqlDatabaseServerContext** cmdlet.</span></span> <span data-ttu-id="b5fbe-160">Aby go usunąć, użyj poleceń podobnych do następujących:</span><span class="sxs-lookup"><span data-stu-id="b5fbe-160">To remove it, use commands similar to the following:</span></span>

  `PS C:\\\> $Credential = Get-Credential`
`PS C:\\\> $Credential = New-Object -TypeName 'System.Management.Automation.PSCredential' -ArgumentList $Credential.Username.Replace("\",""),$Credential.Password`

## <span data-ttu-id="b5fbe-161">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b5fbe-161">RELATED LINKS</span></span>



[<span data-ttu-id="b5fbe-162">Get-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b5fbe-162">Get-AzureSqlDatabase</span></span>](./Get-AzureSqlDatabase.md)

[<span data-ttu-id="b5fbe-163">New-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b5fbe-163">New-AzureSqlDatabase</span></span>](./New-AzureSqlDatabase.md)

[<span data-ttu-id="b5fbe-164">Remove-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b5fbe-164">Remove-AzureSqlDatabase</span></span>](./Remove-AzureSqlDatabase.md)

[<span data-ttu-id="b5fbe-165">Set-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b5fbe-165">Set-AzureSqlDatabase</span></span>](./Set-AzureSqlDatabase.md)


