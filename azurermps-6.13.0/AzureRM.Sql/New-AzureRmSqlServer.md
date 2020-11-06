---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 7039528F-42AE-45DB-BF81-FE5003F8AEE2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServer.md
ms.openlocfilehash: 208d72607397cb61e098052cd1835f44d4e0e4a5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546411"
---
# <span data-ttu-id="86c78-101">New-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="86c78-101">New-AzureRmSqlServer</span></span>

## <span data-ttu-id="86c78-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="86c78-102">SYNOPSIS</span></span>
<span data-ttu-id="86c78-103">Tworzy serwer bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="86c78-103">Creates a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="86c78-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="86c78-104">SYNTAX</span></span>

```
New-AzureRmSqlServer -ServerName <String> -SqlAdministratorCredentials <PSCredential> -Location <String>
 [-Tags <Hashtable>] [-ServerVersion <String>] [-AssignIdentity] [-AsJob] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86c78-105">Opis</span><span class="sxs-lookup"><span data-stu-id="86c78-105">DESCRIPTION</span></span>
<span data-ttu-id="86c78-106">Polecenie cmdlet **New-AzureRmSqlServer** umożliwia utworzenie serwera bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="86c78-106">The **New-AzureRmSqlServer** cmdlet creates an Azure SQL Database server.</span></span>

## <span data-ttu-id="86c78-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="86c78-107">EXAMPLES</span></span>

### <span data-ttu-id="86c78-108">Przykład 1. Tworzenie nowego serwera bazy danych SQL Azure</span><span class="sxs-lookup"><span data-stu-id="86c78-108">Example 1: Create a new Azure SQL Database server</span></span>
```
PS C:\>New-AzureRmSqlServer -ResourceGroupName "ResourceGroup01" -Location "Central US" -ServerName "server01" -ServerVersion "12.0" -SqlAdministratorCredentials (Get-Credential)
ResourceGroupName        : resourcegroup01
ServerName               : server01
Location                 : Central US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
```

<span data-ttu-id="86c78-109">To polecenie tworzy serwer bazy danych SQL Azure w wersji 12.</span><span class="sxs-lookup"><span data-stu-id="86c78-109">This command creates a version 12 Azure SQL Database server.</span></span>

## <span data-ttu-id="86c78-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="86c78-110">PARAMETERS</span></span>

### <span data-ttu-id="86c78-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="86c78-111">-AsJob</span></span>
<span data-ttu-id="86c78-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="86c78-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="86c78-113">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="86c78-113">-AssignIdentity</span></span>
<span data-ttu-id="86c78-114">Wygeneruj i przypisz tożsamość usługi Azure Active Directory dla tego serwera do użytku z usługami zarządzania kluczami, takimi jak Magazyn kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="86c78-114">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="86c78-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86c78-115">-DefaultProfile</span></span>
<span data-ttu-id="86c78-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="86c78-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86c78-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="86c78-117">-Location</span></span>
<span data-ttu-id="86c78-118">Określa lokalizację centrum danych, w którym to polecenie cmdlet tworzy serwer.</span><span class="sxs-lookup"><span data-stu-id="86c78-118">Specifies the location of the data center where this cmdlet creates the server.</span></span>

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

### <span data-ttu-id="86c78-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86c78-119">-ResourceGroupName</span></span>
<span data-ttu-id="86c78-120">Określa nazwę grupy zasobów, z którą to polecenie cmdlet przypisze serwerowi.</span><span class="sxs-lookup"><span data-stu-id="86c78-120">Specifies the name of the resource group to which this cmdlet assigns the server.</span></span>

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

### <span data-ttu-id="86c78-121">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="86c78-121">-ServerName</span></span>
<span data-ttu-id="86c78-122">Określa nazwę nowego serwera.</span><span class="sxs-lookup"><span data-stu-id="86c78-122">Specifies the name of the new server.</span></span>

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

### <span data-ttu-id="86c78-123">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="86c78-123">-ServerVersion</span></span>
<span data-ttu-id="86c78-124">Określa wersję nowego serwera.</span><span class="sxs-lookup"><span data-stu-id="86c78-124">Specifies the version of the new server.</span></span> <span data-ttu-id="86c78-125">Dopuszczalne wartości tego parametru to: 2,0 i 12,0.</span><span class="sxs-lookup"><span data-stu-id="86c78-125">The acceptable values for this parameter are: 2.0 and 12.0.</span></span>
<span data-ttu-id="86c78-126">Określ 2,0, aby utworzyć serwer w wersji 11 lub 12,0 w celu utworzenia serwera w wersji 12.</span><span class="sxs-lookup"><span data-stu-id="86c78-126">Specify 2.0 to create a version 11 server, or 12.0 to create a version 12 server.</span></span>

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

### <span data-ttu-id="86c78-127">-SqlAdministratorCredentials</span><span class="sxs-lookup"><span data-stu-id="86c78-127">-SqlAdministratorCredentials</span></span>
<span data-ttu-id="86c78-128">Określa poświadczenia administratora serwera bazy danych SQL dla nowego serwera.</span><span class="sxs-lookup"><span data-stu-id="86c78-128">Specifies the SQL Database server administrator credentials for the new server.</span></span> <span data-ttu-id="86c78-129">Aby uzyskać obiekt **PSCredential** , użyj polecenia cmdlet Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="86c78-129">To obtain a **PSCredential** object, use the Get-Credential cmdlet.</span></span> <span data-ttu-id="86c78-130">Aby uzyskać więcej informacji, wpisz tekst `Get-Help
Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="86c78-130">For more information, type `Get-Help
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

### <span data-ttu-id="86c78-131">-Tagi</span><span class="sxs-lookup"><span data-stu-id="86c78-131">-Tags</span></span>
<span data-ttu-id="86c78-132">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="86c78-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="86c78-133">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="86c78-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="86c78-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="86c78-134">-Confirm</span></span>
<span data-ttu-id="86c78-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="86c78-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86c78-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86c78-136">-WhatIf</span></span>
<span data-ttu-id="86c78-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="86c78-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86c78-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="86c78-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86c78-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86c78-139">CommonParameters</span></span>
<span data-ttu-id="86c78-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86c78-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86c78-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86c78-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86c78-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="86c78-142">INPUTS</span></span>

### <span data-ttu-id="86c78-143">System. String</span><span class="sxs-lookup"><span data-stu-id="86c78-143">System.String</span></span>

## <span data-ttu-id="86c78-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="86c78-144">OUTPUTS</span></span>

### <span data-ttu-id="86c78-145">Microsoft. Azure. Commands. SQL. Server. model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="86c78-145">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="86c78-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="86c78-146">NOTES</span></span>

## <span data-ttu-id="86c78-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="86c78-147">RELATED LINKS</span></span>

[<span data-ttu-id="86c78-148">Get-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="86c78-148">Get-AzureRmSqlServer</span></span>](./Get-AzureRmSqlServer.md)

[<span data-ttu-id="86c78-149">Remove-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="86c78-149">Remove-AzureRmSqlServer</span></span>](./Remove-AzureRmSqlServer.md)

[<span data-ttu-id="86c78-150">Set-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="86c78-150">Set-AzureRmSqlServer</span></span>](./Set-AzureRmSqlServer.md)

[<span data-ttu-id="86c78-151">Nowe — AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="86c78-151">New-AzureRmSqlServerFirewallRule</span></span>](./New-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="86c78-152">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="86c78-152">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
