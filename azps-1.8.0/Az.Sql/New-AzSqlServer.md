---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 7039528F-42AE-45DB-BF81-FE5003F8AEE2
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServer.md
ms.openlocfilehash: 0d5eb08c938fe17e4270cd66038a738341937cb9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707851"
---
# <span data-ttu-id="ceecf-101">New-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="ceecf-101">New-AzSqlServer</span></span>

## <span data-ttu-id="ceecf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ceecf-102">SYNOPSIS</span></span>
<span data-ttu-id="ceecf-103">Tworzy serwer bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="ceecf-103">Creates a SQL Database server.</span></span>

## <span data-ttu-id="ceecf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ceecf-104">SYNTAX</span></span>

```
New-AzSqlServer -ServerName <String> -SqlAdministratorCredentials <PSCredential> -Location <String>
 [-Tags <Hashtable>] [-ServerVersion <String>] [-AssignIdentity] [-AsJob] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ceecf-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ceecf-105">DESCRIPTION</span></span>
<span data-ttu-id="ceecf-106">Polecenie cmdlet **New-AzSqlServer** umożliwia utworzenie serwera bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="ceecf-106">The **New-AzSqlServer** cmdlet creates an Azure SQL Database server.</span></span>

## <span data-ttu-id="ceecf-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ceecf-107">EXAMPLES</span></span>

### <span data-ttu-id="ceecf-108">Przykład 1. Tworzenie nowego serwera bazy danych SQL Azure</span><span class="sxs-lookup"><span data-stu-id="ceecf-108">Example 1: Create a new Azure SQL Database server</span></span>
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

<span data-ttu-id="ceecf-109">To polecenie tworzy serwer bazy danych SQL Azure w wersji 12.</span><span class="sxs-lookup"><span data-stu-id="ceecf-109">This command creates a version 12 Azure SQL Database server.</span></span>

## <span data-ttu-id="ceecf-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ceecf-110">PARAMETERS</span></span>

### <span data-ttu-id="ceecf-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ceecf-111">-AsJob</span></span>
<span data-ttu-id="ceecf-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="ceecf-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ceecf-113">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="ceecf-113">-AssignIdentity</span></span>
<span data-ttu-id="ceecf-114">Wygeneruj i przypisz tożsamość usługi Azure Active Directory dla tego serwera do użytku z usługami zarządzania kluczami, takimi jak Magazyn kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ceecf-114">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="ceecf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ceecf-115">-DefaultProfile</span></span>
<span data-ttu-id="ceecf-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="ceecf-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ceecf-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="ceecf-117">-Location</span></span>
<span data-ttu-id="ceecf-118">Określa lokalizację centrum danych, w którym to polecenie cmdlet tworzy serwer.</span><span class="sxs-lookup"><span data-stu-id="ceecf-118">Specifies the location of the data center where this cmdlet creates the server.</span></span>

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

### <span data-ttu-id="ceecf-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ceecf-119">-ResourceGroupName</span></span>
<span data-ttu-id="ceecf-120">Określa nazwę grupy zasobów, z którą to polecenie cmdlet przypisze serwerowi.</span><span class="sxs-lookup"><span data-stu-id="ceecf-120">Specifies the name of the resource group to which this cmdlet assigns the server.</span></span>

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

### <span data-ttu-id="ceecf-121">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="ceecf-121">-ServerName</span></span>
<span data-ttu-id="ceecf-122">Określa nazwę nowego serwera.</span><span class="sxs-lookup"><span data-stu-id="ceecf-122">Specifies the name of the new server.</span></span>

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

### <span data-ttu-id="ceecf-123">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="ceecf-123">-ServerVersion</span></span>
<span data-ttu-id="ceecf-124">Określa wersję nowego serwera.</span><span class="sxs-lookup"><span data-stu-id="ceecf-124">Specifies the version of the new server.</span></span> <span data-ttu-id="ceecf-125">Dopuszczalne wartości tego parametru to: 2,0 i 12,0.</span><span class="sxs-lookup"><span data-stu-id="ceecf-125">The acceptable values for this parameter are: 2.0 and 12.0.</span></span>
<span data-ttu-id="ceecf-126">Określ 2,0, aby utworzyć serwer w wersji 11 lub 12,0 w celu utworzenia serwera w wersji 12.</span><span class="sxs-lookup"><span data-stu-id="ceecf-126">Specify 2.0 to create a version 11 server, or 12.0 to create a version 12 server.</span></span>

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

### <span data-ttu-id="ceecf-127">-SqlAdministratorCredentials</span><span class="sxs-lookup"><span data-stu-id="ceecf-127">-SqlAdministratorCredentials</span></span>
<span data-ttu-id="ceecf-128">Określa poświadczenia administratora serwera bazy danych SQL dla nowego serwera.</span><span class="sxs-lookup"><span data-stu-id="ceecf-128">Specifies the SQL Database server administrator credentials for the new server.</span></span> <span data-ttu-id="ceecf-129">Aby uzyskać obiekt **PSCredential** , użyj polecenia cmdlet Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="ceecf-129">To obtain a **PSCredential** object, use the Get-Credential cmdlet.</span></span> <span data-ttu-id="ceecf-130">Aby uzyskać więcej informacji, wpisz tekst `Get-Help
Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="ceecf-130">For more information, type `Get-Help
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

### <span data-ttu-id="ceecf-131">-Tagi</span><span class="sxs-lookup"><span data-stu-id="ceecf-131">-Tags</span></span>
<span data-ttu-id="ceecf-132">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="ceecf-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="ceecf-133">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="ceecf-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="ceecf-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ceecf-134">-Confirm</span></span>
<span data-ttu-id="ceecf-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ceecf-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ceecf-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ceecf-136">-WhatIf</span></span>
<span data-ttu-id="ceecf-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ceecf-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ceecf-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ceecf-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ceecf-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ceecf-139">CommonParameters</span></span>
<span data-ttu-id="ceecf-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ceecf-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ceecf-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ceecf-141">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ceecf-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ceecf-142">INPUTS</span></span>

### <span data-ttu-id="ceecf-143">System. String</span><span class="sxs-lookup"><span data-stu-id="ceecf-143">System.String</span></span>

## <span data-ttu-id="ceecf-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ceecf-144">OUTPUTS</span></span>

### <span data-ttu-id="ceecf-145">Microsoft. Azure. Commands. SQL. Server. model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="ceecf-145">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="ceecf-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ceecf-146">NOTES</span></span>

## <span data-ttu-id="ceecf-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ceecf-147">RELATED LINKS</span></span>

[<span data-ttu-id="ceecf-148">Get-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="ceecf-148">Get-AzSqlServer</span></span>](./Get-AzSqlServer.md)

[<span data-ttu-id="ceecf-149">Remove-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="ceecf-149">Remove-AzSqlServer</span></span>](./Remove-AzSqlServer.md)

[<span data-ttu-id="ceecf-150">Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="ceecf-150">Set-AzSqlServer</span></span>](./Set-AzSqlServer.md)

[<span data-ttu-id="ceecf-151">Nowe — AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="ceecf-151">New-AzSqlServerFirewallRule</span></span>](./New-AzSqlServerFirewallRule.md)

[<span data-ttu-id="ceecf-152">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="ceecf-152">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
