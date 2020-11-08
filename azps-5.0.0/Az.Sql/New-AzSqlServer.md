---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 7039528F-42AE-45DB-BF81-FE5003F8AEE2
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServer.md
ms.openlocfilehash: ec2e71e6556824ad92e1a5839f0b10c91960fec0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94225634"
---
# <span data-ttu-id="9ff00-101">New-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="9ff00-101">New-AzSqlServer</span></span>

## <span data-ttu-id="9ff00-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9ff00-102">SYNOPSIS</span></span>
<span data-ttu-id="9ff00-103">Tworzy serwer bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="9ff00-103">Creates a SQL Database server.</span></span>

## <span data-ttu-id="9ff00-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9ff00-104">SYNTAX</span></span>

```
New-AzSqlServer -ServerName <String> -SqlAdministratorCredentials <PSCredential> -Location <String>
 [-Tags <Hashtable>] [-ServerVersion <String>] [-AssignIdentity] [-PublicNetworkAccess <String>]
 [-MinimalTlsVersion <String>] [-AsJob] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ff00-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9ff00-105">DESCRIPTION</span></span>
<span data-ttu-id="9ff00-106">Polecenie cmdlet **New-AzSqlServer** umożliwia utworzenie serwera bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="9ff00-106">The **New-AzSqlServer** cmdlet creates an Azure SQL Database server.</span></span>

## <span data-ttu-id="9ff00-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9ff00-107">EXAMPLES</span></span>

### <span data-ttu-id="9ff00-108">Przykład 1. Tworzenie nowego serwera bazy danych SQL Azure</span><span class="sxs-lookup"><span data-stu-id="9ff00-108">Example 1: Create a new Azure SQL Database server</span></span>
```
PS C:\>New-AzSqlServer -ResourceGroupName "ResourceGroup01" -Location "Central US" -ServerName "server01" -ServerVersion "12.0" -SqlAdministratorCredentials (Get-Credential)
ResourceGroupName        : resourcegroup01
ServerName               : server01
Location                 : Central US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
```

<span data-ttu-id="9ff00-109">To polecenie tworzy serwer bazy danych SQL Azure w wersji 12.</span><span class="sxs-lookup"><span data-stu-id="9ff00-109">This command creates a version 12 Azure SQL Database server.</span></span>

## <span data-ttu-id="9ff00-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9ff00-110">PARAMETERS</span></span>

### <span data-ttu-id="9ff00-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9ff00-111">-AsJob</span></span>
<span data-ttu-id="9ff00-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="9ff00-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9ff00-113">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="9ff00-113">-AssignIdentity</span></span>
<span data-ttu-id="9ff00-114">Wygeneruj i przypisz tożsamość usługi Azure Active Directory dla tego serwera do użytku z usługami zarządzania kluczami, takimi jak Magazyn kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9ff00-114">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="9ff00-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ff00-115">-DefaultProfile</span></span>
<span data-ttu-id="9ff00-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="9ff00-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9ff00-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="9ff00-117">-Location</span></span>
<span data-ttu-id="9ff00-118">Określa lokalizację centrum danych, w którym to polecenie cmdlet tworzy serwer.</span><span class="sxs-lookup"><span data-stu-id="9ff00-118">Specifies the location of the data center where this cmdlet creates the server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ff00-119">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="9ff00-119">-MinimalTlsVersion</span></span>
<span data-ttu-id="9ff00-120">Wersja minimalnego szyfrowania TLS do wymuszania dla programu SQL Server</span><span class="sxs-lookup"><span data-stu-id="9ff00-120">The minimal TLS version to enforce for Sql Server</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: 1.0, 1.1, 1.2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ff00-121">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="9ff00-121">-PublicNetworkAccess</span></span>
<span data-ttu-id="9ff00-122">Umożliwia określenie, czy dostęp do serwera jest dozwolony w sieci publicznej, czy jest włączony i wyłączony.</span><span class="sxs-lookup"><span data-stu-id="9ff00-122">Takes a flag, enabled/disabled, to specify whether public network access to server is allowed or not.</span></span>
<span data-ttu-id="9ff00-123">Po wyłączeniu tego serwera mogą się łączyć tylko połączenia realizowane za pośrednictwem linków prywatnych.</span><span class="sxs-lookup"><span data-stu-id="9ff00-123">When disabled, only connections made through Private Links can reach this server.</span></span>

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

### <span data-ttu-id="9ff00-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ff00-124">-ResourceGroupName</span></span>
<span data-ttu-id="9ff00-125">Określa nazwę grupy zasobów, z którą to polecenie cmdlet przypisze serwerowi.</span><span class="sxs-lookup"><span data-stu-id="9ff00-125">Specifies the name of the resource group to which this cmdlet assigns the server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ff00-126">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="9ff00-126">-ServerName</span></span>
<span data-ttu-id="9ff00-127">Określa nazwę nowego serwera.</span><span class="sxs-lookup"><span data-stu-id="9ff00-127">Specifies the name of the new server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ff00-128">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="9ff00-128">-ServerVersion</span></span>
<span data-ttu-id="9ff00-129">Określa wersję nowego serwera.</span><span class="sxs-lookup"><span data-stu-id="9ff00-129">Specifies the version of the new server.</span></span> <span data-ttu-id="9ff00-130">Dopuszczalne wartości tego parametru to: 2,0 i 12,0.</span><span class="sxs-lookup"><span data-stu-id="9ff00-130">The acceptable values for this parameter are: 2.0 and 12.0.</span></span>
<span data-ttu-id="9ff00-131">Określ 2,0, aby utworzyć serwer w wersji 11 lub 12,0 w celu utworzenia serwera w wersji 12.</span><span class="sxs-lookup"><span data-stu-id="9ff00-131">Specify 2.0 to create a version 11 server, or 12.0 to create a version 12 server.</span></span>

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

### <span data-ttu-id="9ff00-132">-SqlAdministratorCredentials</span><span class="sxs-lookup"><span data-stu-id="9ff00-132">-SqlAdministratorCredentials</span></span>
<span data-ttu-id="9ff00-133">Określa poświadczenia administratora serwera bazy danych SQL dla nowego serwera.</span><span class="sxs-lookup"><span data-stu-id="9ff00-133">Specifies the SQL Database server administrator credentials for the new server.</span></span> <span data-ttu-id="9ff00-134">Aby uzyskać obiekt **PSCredential** , użyj polecenia cmdlet Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="9ff00-134">To obtain a **PSCredential** object, use the Get-Credential cmdlet.</span></span> <span data-ttu-id="9ff00-135">Aby uzyskać więcej informacji, wpisz tekst `Get-Help
Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="9ff00-135">For more information, type `Get-Help
Get-Credential`.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ff00-136">-Tagi</span><span class="sxs-lookup"><span data-stu-id="9ff00-136">-Tags</span></span>
<span data-ttu-id="9ff00-137">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="9ff00-137">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="9ff00-138">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="9ff00-138">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ff00-139">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9ff00-139">-Confirm</span></span>
<span data-ttu-id="9ff00-140">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9ff00-140">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ff00-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ff00-141">-WhatIf</span></span>
<span data-ttu-id="9ff00-142">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9ff00-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ff00-143">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9ff00-143">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ff00-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ff00-144">CommonParameters</span></span>
<span data-ttu-id="9ff00-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ff00-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ff00-146">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9ff00-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ff00-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9ff00-147">INPUTS</span></span>

### <span data-ttu-id="9ff00-148">System. String</span><span class="sxs-lookup"><span data-stu-id="9ff00-148">System.String</span></span>

## <span data-ttu-id="9ff00-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9ff00-149">OUTPUTS</span></span>

### <span data-ttu-id="9ff00-150">Microsoft. Azure. Commands. SQL. Server. model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="9ff00-150">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="9ff00-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9ff00-151">NOTES</span></span>

## <span data-ttu-id="9ff00-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9ff00-152">RELATED LINKS</span></span>

[<span data-ttu-id="9ff00-153">Get-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="9ff00-153">Get-AzSqlServer</span></span>](./Get-AzSqlServer.md)

[<span data-ttu-id="9ff00-154">Remove-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="9ff00-154">Remove-AzSqlServer</span></span>](./Remove-AzSqlServer.md)

[<span data-ttu-id="9ff00-155">Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="9ff00-155">Set-AzSqlServer</span></span>](./Set-AzSqlServer.md)

[<span data-ttu-id="9ff00-156">Nowe — AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="9ff00-156">New-AzSqlServerFirewallRule</span></span>](./New-AzSqlServerFirewallRule.md)

[<span data-ttu-id="9ff00-157">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="9ff00-157">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
