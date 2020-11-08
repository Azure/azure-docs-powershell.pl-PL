---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: B7B29875-D2E5-4E96-AD4B-83032AB18D02
online version: ''
schema: 2.0.0
ms.openlocfilehash: cdcd4788e3eefdce858cb88c0bf1885353f8a673
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054936"
---
# <span data-ttu-id="7da89-101">New-AzureSqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="7da89-101">New-AzureSqlDatabaseServerContext</span></span>

## <span data-ttu-id="7da89-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7da89-102">SYNOPSIS</span></span>
<span data-ttu-id="7da89-103">Tworzy kontekst połączenia z serwerem.</span><span class="sxs-lookup"><span data-stu-id="7da89-103">Creates a server connection context.</span></span>

## <span data-ttu-id="7da89-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7da89-104">SYNTAX</span></span>

### <span data-ttu-id="7da89-105">ByServerNameWithSqlAuth (domyślny)</span><span class="sxs-lookup"><span data-stu-id="7da89-105">ByServerNameWithSqlAuth (Default)</span></span>
```
New-AzureSqlDatabaseServerContext -ServerName <String> -Credential <PSCredential> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="7da89-106">ByManageUrlWithSqlAuth</span><span class="sxs-lookup"><span data-stu-id="7da89-106">ByManageUrlWithSqlAuth</span></span>
```
New-AzureSqlDatabaseServerContext [-ServerName <String>] -ManageUrl <Uri> -Credential <PSCredential>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="7da89-107">ByServerNameWithCertAuth</span><span class="sxs-lookup"><span data-stu-id="7da89-107">ByServerNameWithCertAuth</span></span>
```
New-AzureSqlDatabaseServerContext -ServerName <String> [-UseSubscription] [-SubscriptionName <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="7da89-108">ByFullyQualifiedServerNameWithSqlAuth</span><span class="sxs-lookup"><span data-stu-id="7da89-108">ByFullyQualifiedServerNameWithSqlAuth</span></span>
```
New-AzureSqlDatabaseServerContext -FullyQualifiedServerName <String> -Credential <PSCredential>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="7da89-109">ByFullyQualifiedServerNameWithCertAuth</span><span class="sxs-lookup"><span data-stu-id="7da89-109">ByFullyQualifiedServerNameWithCertAuth</span></span>
```
New-AzureSqlDatabaseServerContext -FullyQualifiedServerName <String> [-UseSubscription]
 [-SubscriptionName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="7da89-110">Opis</span><span class="sxs-lookup"><span data-stu-id="7da89-110">DESCRIPTION</span></span>
<span data-ttu-id="7da89-111">Polecenie cmdlet **New-AzureSqlDatabaseServerContext** służy do tworzenia kontekstu połączenia serwera bazy danych Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="7da89-111">The **New-AzureSqlDatabaseServerContext** cmdlet creates an Azure SQL Database server connection context.</span></span>
<span data-ttu-id="7da89-112">Użyj uwierzytelniania programu SQL Server, aby utworzyć kontekst połączenia z serwerem bazy danych SQL, używając określonych poświadczeń.</span><span class="sxs-lookup"><span data-stu-id="7da89-112">Use SQL Server authentication to create a connection context to a SQL Database server by using the specified credentials.</span></span>
<span data-ttu-id="7da89-113">Możesz określić serwer bazy danych SQL według nazwy, w pełni kwalifikowanej nazwy lub według adresu URL.</span><span class="sxs-lookup"><span data-stu-id="7da89-113">You can specify the SQL Database server by name, by the fully qualified name, or by URL.</span></span>
<span data-ttu-id="7da89-114">Aby uzyskać poświadczenie, użyj polecenia cmdlet Get-Credential, w którym jest wyświetlany monit o określenie nazwy użytkownika i hasła.</span><span class="sxs-lookup"><span data-stu-id="7da89-114">To obtain a credential, use the Get-Credential cmdlet that prompts you to specify the user name and password.</span></span>

<span data-ttu-id="7da89-115">Użyj polecenia cmdlet **New-AzureSqlDatabaseServerContext** z uwierzytelnianiem opartym na certyfikatach, aby utworzyć kontekst połączenia dla określonego serwera bazy danych SQL, używając określonych danych subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="7da89-115">Use the **New-AzureSqlDatabaseServerContext** cmdlet with certificate based authentication to create a connection context to the specified SQL Database server by using the specified Azure subscription data.</span></span>
<span data-ttu-id="7da89-116">Możesz określić serwer bazy danych SQL według nazwy lub w pełni kwalifikowanej nazwy.</span><span class="sxs-lookup"><span data-stu-id="7da89-116">You can specify SQL Database server by name or by the fully qualified name.</span></span>
<span data-ttu-id="7da89-117">Możesz określić dane abonamentu jako parametr lub można go pobrać z bieżącej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="7da89-117">You can specify the subscription data as a parameter or it can be retrieved from the current Azure subscription.</span></span>
<span data-ttu-id="7da89-118">Użyj polecenia cmdlet Select-AzureSubscription https://msdn.microsoft.com/library/windowsazure/jj152833.aspx w celu wybrania bieżącej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="7da89-118">Use the Select-AzureSubscriptionhttps://msdn.microsoft.com/library/windowsazure/jj152833.aspx cmdlet to select the current Azure subscription.</span></span>

## <span data-ttu-id="7da89-119">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7da89-119">EXAMPLES</span></span>

### <span data-ttu-id="7da89-120">Przykład 1. Tworzenie kontekstu za pomocą uwierzytelniania programu SQL Server</span><span class="sxs-lookup"><span data-stu-id="7da89-120">Example 1: Create a context by using SQL Server authentication</span></span>
```
PS C:\> $Credential = Get-Credential
PS C:\> $Context = New-AzureSqlDatabaseServerContext -ServerName "lpqd0zbr8y" -Credential $Credential
PS C:\> $Database17 = New-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database17" -MaxSizeGB 50 -Collation "SQL_Latin1_General_CP1_CI_AS"
```

<span data-ttu-id="7da89-121">W tym przykładzie użyto uwierzytelniania programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="7da89-121">This example uses the SQL Server authentication.</span></span>

<span data-ttu-id="7da89-122">Pierwsze polecenie monituje o podanie poświadczeń administratora serwera i zapisuje poświadczenia w zmiennej $Credential.</span><span class="sxs-lookup"><span data-stu-id="7da89-122">The first command prompts you for server administrator credentials, and stores the credentials in the $Credential variable.</span></span>

<span data-ttu-id="7da89-123">Drugie polecenie nawiązuje połączenie z serwerem bazy danych SQL o nazwie lpqd0zbr8y przy użyciu $Credential.</span><span class="sxs-lookup"><span data-stu-id="7da89-123">The second command connects to the SQL Database server named lpqd0zbr8y by using $Credential.</span></span>

<span data-ttu-id="7da89-124">Polecenie ostatnie tworzy bazę danych o nazwie Database17 na serwerze, który jest częścią kontekstu w $Context.</span><span class="sxs-lookup"><span data-stu-id="7da89-124">The final command creates a database named Database17 on the server that is part of the context in $Context.</span></span>

### <span data-ttu-id="7da89-125">Przykład 2: Tworzenie kontekstu przy użyciu uwierzytelniania opartego na certyfikatach</span><span class="sxs-lookup"><span data-stu-id="7da89-125">Example 2: Create a context by using certificate based authentication</span></span>
```
PS C:\> $SubscriptionId = <Subscription ID>
PS C:\> $Thumbprint = <Certificate Thumbprint>
PS C:\> $Certificate = Get-Item "Cert:\CurrentUser\My\$Thumbprint"
PS C:\> Set-AzureSubscription -SubscriptionName "Subscription07" -SubscriptionId $SubscriptionId -Certificate $Certificate
PS C:\> Select-AzureSubscription -SubscriptionName "Subscription07"
PS C:\> $Context = New-AzureSqlDatabaseServerContext -ServerName "lpqd0zbr8y" -UseSubscription
```

<span data-ttu-id="7da89-126">W tym przykładzie użyto uwierzytelniania opartego na certyfikatach.</span><span class="sxs-lookup"><span data-stu-id="7da89-126">This example uses the certificate based authentication.</span></span>

<span data-ttu-id="7da89-127">Pierwsze dwa polecenia przypisują wartości do zmiennych $SubscriptionId i $Thumbprint.</span><span class="sxs-lookup"><span data-stu-id="7da89-127">The first two commands assign values to the $SubscriptionId and $Thumbprint variables.</span></span>

<span data-ttu-id="7da89-128">Trzecia komenda uzyskuje certyfikat zidentyfikowany przez odcisk palca w $Thumbprint i zapisuje go w $Certificate.</span><span class="sxs-lookup"><span data-stu-id="7da89-128">The third command gets the certificate identified by the thumbprint in $Thumbprint, and stores it in $Certificate.</span></span>

<span data-ttu-id="7da89-129">Czwarte polecenie ustawia abonament na Subscription07, a w piątym poleceniu jest wybrana ta subskrypcja.</span><span class="sxs-lookup"><span data-stu-id="7da89-129">The fourth command sets the subscription to be Subscription07, and the fifth command selects that subscription.</span></span>

<span data-ttu-id="7da89-130">Polecenie ostatnie powoduje utworzenie kontekstu w bieżącej subskrypcji dla serwera o nazwie lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="7da89-130">The final command creates a context in the current subscription for the server named lpqd0zbr8y.</span></span>

## <span data-ttu-id="7da89-131">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7da89-131">PARAMETERS</span></span>

### <span data-ttu-id="7da89-132">— Poświadczenie</span><span class="sxs-lookup"><span data-stu-id="7da89-132">-Credential</span></span>
<span data-ttu-id="7da89-133">Określa obiekt poświadczeń, który umożliwia uwierzytelnianie programu SQL Server w celu uzyskania dostępu do serwera.</span><span class="sxs-lookup"><span data-stu-id="7da89-133">Specifies a credential object that provides SQL Server authentication for you to access the server.</span></span>

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

### <span data-ttu-id="7da89-134">-FullyQualifiedServerName</span><span class="sxs-lookup"><span data-stu-id="7da89-134">-FullyQualifiedServerName</span></span>
<span data-ttu-id="7da89-135">Określa w pełni kwalifikowaną nazwę domeny (FQDN) dla serwera bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="7da89-135">Specifies the fully qualified domain name (FQDN) name for the Azure SQL Database server.</span></span>
<span data-ttu-id="7da89-136">Na przykład Server02.database.windows.net.</span><span class="sxs-lookup"><span data-stu-id="7da89-136">For example, Server02.database.windows.net.</span></span>

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

### <span data-ttu-id="7da89-137">-ManageUrl</span><span class="sxs-lookup"><span data-stu-id="7da89-137">-ManageUrl</span></span>
<span data-ttu-id="7da89-138">Określa adres URL używany przez ten aplet polecenia w celu uzyskania dostępu do portalu usługi Azure SQL DatabaseManagement dla serwera.</span><span class="sxs-lookup"><span data-stu-id="7da89-138">Specifies the URL that this cmdlet uses to access the Azure SQL DatabaseManagement Portal for the server.</span></span>

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

### <span data-ttu-id="7da89-139">-Profile</span><span class="sxs-lookup"><span data-stu-id="7da89-139">-Profile</span></span>
<span data-ttu-id="7da89-140">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7da89-140">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7da89-141">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="7da89-141">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7da89-142">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="7da89-142">-ServerName</span></span>
<span data-ttu-id="7da89-143">Określa nazwę serwera bazy danych.</span><span class="sxs-lookup"><span data-stu-id="7da89-143">Specifies the name of the database server.</span></span>

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

### <span data-ttu-id="7da89-144">-Subscriptionname</span><span class="sxs-lookup"><span data-stu-id="7da89-144">-SubscriptionName</span></span>
<span data-ttu-id="7da89-145">Określa nazwę subskrypcji platformy Azure używanej przez to polecenie cmdlet do tworzenia kontekstu połączenia.</span><span class="sxs-lookup"><span data-stu-id="7da89-145">Specifies the name of the Azure subscription that this cmdlet uses to create the connection context.</span></span>
<span data-ttu-id="7da89-146">Jeśli nie określisz wartości dla tego parametru, polecenie cmdlet użyje bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="7da89-146">If you do not specify a value for this parameter, the cmdlet uses the current subscription.</span></span>
<span data-ttu-id="7da89-147">Uruchom polecenie cmdlet Select-AzureSubscription, aby zmienić bieżącą subskrypcję.</span><span class="sxs-lookup"><span data-stu-id="7da89-147">Run the Select-AzureSubscription cmdlet to change the current subscription.</span></span>

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

### <span data-ttu-id="7da89-148">-UseSubscription</span><span class="sxs-lookup"><span data-stu-id="7da89-148">-UseSubscription</span></span>
<span data-ttu-id="7da89-149">Wskazuje, że w tym poleceniu cmdlet jest używany abonament platformy Azure służący do tworzenia kontekstu połączenia.</span><span class="sxs-lookup"><span data-stu-id="7da89-149">Indicates that this cmdlet uses Azure subscription for creating the connection context.</span></span>

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

### <span data-ttu-id="7da89-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7da89-150">CommonParameters</span></span>
<span data-ttu-id="7da89-151">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7da89-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7da89-152">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7da89-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7da89-153">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7da89-153">INPUTS</span></span>

## <span data-ttu-id="7da89-154">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7da89-154">OUTPUTS</span></span>

### <span data-ttu-id="7da89-155">Microsoft. platformy windowsazure. Commands. SQLDatabase. Services. Server. IServerDataServiceContext</span><span class="sxs-lookup"><span data-stu-id="7da89-155">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.IServerDataServiceContext</span></span>

## <span data-ttu-id="7da89-156">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7da89-156">NOTES</span></span>
* <span data-ttu-id="7da89-157">Jeśli uwierzytelniasz bez określania domeny, a jeśli korzystasz z programu Windows PowerShell 2,0, polecenie cmdlet Get-Credential zwraca ukośnik odwrotny ( \\ ) poprzedzony znakiem username (), na przykład \User.</span><span class="sxs-lookup"><span data-stu-id="7da89-157">If you authenticate without specifying a domain, and if you use Windows PowerShell 2.0, the Get-Credential cmdlet returns a backslash (\\) prepended to the username, for example, \user.</span></span> <span data-ttu-id="7da89-158">Program Windows PowerShell 3,0 nie dodaje ukośnika odwrotnego.</span><span class="sxs-lookup"><span data-stu-id="7da89-158">Windows PowerShell 3.0 does not add the backslash.</span></span> <span data-ttu-id="7da89-159">Ten ukośnik nie jest rozpoznawany przez parametr *Credential* polecenia cmdlet **New-AzureSqlDatabaseServerContext** .</span><span class="sxs-lookup"><span data-stu-id="7da89-159">This backslash is not recognized by the *Credential* parameter of the **New-AzureSqlDatabaseServerContext** cmdlet.</span></span> <span data-ttu-id="7da89-160">Aby ją usunąć, Użyj poleceń podobnych do następujących:</span><span class="sxs-lookup"><span data-stu-id="7da89-160">To remove it, use commands similar to the following:</span></span>

  `PS C:\\\> $Credential = Get-Credential`
`PS C:\\\> $Credential = New-Object -TypeName 'System.Management.Automation.PSCredential' -ArgumentList $Credential.Username.Replace("\",""),$Credential.Password`

## <span data-ttu-id="7da89-161">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7da89-161">RELATED LINKS</span></span>

[<span data-ttu-id="7da89-162">Polecenia cmdlet usługi Azure SQL Database</span><span class="sxs-lookup"><span data-stu-id="7da89-162">Azure SQL Database Cmdlets</span></span>](./Azure.SQLDatabase.md)

[<span data-ttu-id="7da89-163">Get-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="7da89-163">Get-AzureSqlDatabase</span></span>](./Get-AzureSqlDatabase.md)

[<span data-ttu-id="7da89-164">Nowe — AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="7da89-164">New-AzureSqlDatabase</span></span>](./New-AzureSqlDatabase.md)

[<span data-ttu-id="7da89-165">Remove-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="7da89-165">Remove-AzureSqlDatabase</span></span>](./Remove-AzureSqlDatabase.md)

[<span data-ttu-id="7da89-166">Set-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="7da89-166">Set-AzureSqlDatabase</span></span>](./Set-AzureSqlDatabase.md)


