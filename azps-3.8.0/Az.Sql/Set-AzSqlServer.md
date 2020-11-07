---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: FAAF458C-1662-4130-9A16-0514B714D11D
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServer.md
ms.openlocfilehash: f408edfa0bcdff88fe7577a7cdb6549dcd722dc2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93894477"
---
# <span data-ttu-id="65a43-101">Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="65a43-101">Set-AzSqlServer</span></span>

## <span data-ttu-id="65a43-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="65a43-102">SYNOPSIS</span></span>
<span data-ttu-id="65a43-103">Modyfikuje właściwości serwera bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="65a43-103">Modifies properties of a SQL Database server.</span></span>

## <span data-ttu-id="65a43-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="65a43-104">SYNTAX</span></span>

```
Set-AzSqlServer [-ServerName] <String> [-SqlAdministratorPassword <SecureString>] [-Tags <Hashtable>]
 [-ServerVersion <String>] [-AssignIdentity] [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-MinimalTlsVersion <String>] [-PublicNetworkAccess <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65a43-105">Opis</span><span class="sxs-lookup"><span data-stu-id="65a43-105">DESCRIPTION</span></span>
<span data-ttu-id="65a43-106">Polecenie cmdlet **Set-AzSqlServer** modyfikuje właściwości serwera bazy danych Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="65a43-106">The **Set-AzSqlServer** cmdlet modifies properties of an Azure SQL Database server.</span></span>

## <span data-ttu-id="65a43-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="65a43-107">EXAMPLES</span></span>

### <span data-ttu-id="65a43-108">Przykład 1: Resetowanie hasła administratora</span><span class="sxs-lookup"><span data-stu-id="65a43-108">Example 1: Reset the administrator password</span></span>
```
PS C:\>$ServerPassword = "newpassword"
PS C:\> $SecureString = ConvertTo-SecureString $ServerPassword -AsPlainText -Force
PS C:\> Set-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -SqlAdministratorPassword $secureString
ResourceGroupName        : ResourceGroup01
ServerName               : Server01
Location                 : Australia East
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
Identity                 :
FullyQualifiedDomainName : server01.database.windows.net
```

<span data-ttu-id="65a43-109">To polecenie resetuje hasło administratora na serwerze AzureSQL o nazwie Server01.</span><span class="sxs-lookup"><span data-stu-id="65a43-109">This command resets the administrator password on the AzureSQL Server named server01.</span></span>

## <span data-ttu-id="65a43-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="65a43-110">PARAMETERS</span></span>

### <span data-ttu-id="65a43-111">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="65a43-111">-AssignIdentity</span></span>
<span data-ttu-id="65a43-112">Wygeneruj i przypisz tożsamość usługi Azure Active Directory dla tego serwera do użytku z usługami zarządzania kluczami, takimi jak Magazyn kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="65a43-112">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="65a43-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65a43-113">-DefaultProfile</span></span>
<span data-ttu-id="65a43-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="65a43-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="65a43-115">-Force</span><span class="sxs-lookup"><span data-stu-id="65a43-115">-Force</span></span>
<span data-ttu-id="65a43-116">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="65a43-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="65a43-117">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="65a43-117">-PublicNetworkAccess</span></span>
<span data-ttu-id="65a43-118">Umożliwia określenie, czy dostęp do serwera jest dozwolony w sieci publicznej, czy jest włączony i wyłączony.</span><span class="sxs-lookup"><span data-stu-id="65a43-118">Takes a flag, enabled/disabled, to specify whether public network access to server is allowed or not.</span></span>
<span data-ttu-id="65a43-119">Po wyłączeniu tego serwera mogą się łączyć tylko połączenia realizowane za pośrednictwem linków prywatnych.</span><span class="sxs-lookup"><span data-stu-id="65a43-119">When disabled, only connections made through Private Links can reach this server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65a43-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65a43-120">-ResourceGroupName</span></span>
<span data-ttu-id="65a43-121">Określa nazwę grupy zasobów, do której jest przypisany serwer.</span><span class="sxs-lookup"><span data-stu-id="65a43-121">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="65a43-122">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="65a43-122">-ServerName</span></span>
<span data-ttu-id="65a43-123">Określa nazwę serwera, który jest modyfikowany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65a43-123">Specifies the name of the server that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65a43-124">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="65a43-124">-ServerVersion</span></span>
<span data-ttu-id="65a43-125">Określa wersję, do której to polecenie cmdlet zmieni serwer.</span><span class="sxs-lookup"><span data-stu-id="65a43-125">Specifies the version to which this cmdlet changes the server.</span></span> <span data-ttu-id="65a43-126">Dopuszczalne wartości tego parametru to: 2,0 i 12,0.</span><span class="sxs-lookup"><span data-stu-id="65a43-126">The acceptable values for this parameter are: 2.0 and 12.0.</span></span>

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

### <span data-ttu-id="65a43-127">-SqlAdministratorPassword</span><span class="sxs-lookup"><span data-stu-id="65a43-127">-SqlAdministratorPassword</span></span>
<span data-ttu-id="65a43-128">Określa nowe hasło jako element **SecureString** dla administratora serwera bazy danych.</span><span class="sxs-lookup"><span data-stu-id="65a43-128">Specifies a new password, as a **SecureString** , for the database server administrator.</span></span> <span data-ttu-id="65a43-129">Aby uzyskać element **SecureString** , użyj polecenia cmdlet Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="65a43-129">To obtain a **SecureString** , use the Get-Credential cmdlet.</span></span> <span data-ttu-id="65a43-130">Aby uzyskać więcej informacji, wpisz tekst `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="65a43-130">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65a43-131">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="65a43-131">-MinimalTlsVersion</span></span>
<span data-ttu-id="65a43-132">Wersja minimalnego szyfrowania TLS do wymuszania dla programu SQL Server</span><span class="sxs-lookup"><span data-stu-id="65a43-132">The minimal TLS version to enforce for Sql Server</span></span>

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

### <span data-ttu-id="65a43-133">-Tagi</span><span class="sxs-lookup"><span data-stu-id="65a43-133">-Tags</span></span>
<span data-ttu-id="65a43-134">Określa słownik tagów, które to polecenie cmdlet kojarzy z serwerem.</span><span class="sxs-lookup"><span data-stu-id="65a43-134">Specifies a dictionary of tags that this cmdlet associates with the server.</span></span> <span data-ttu-id="65a43-135">Pary klucz-wartość w formie tabeli skrótów ustawione jako znaczniki na serwerze.</span><span class="sxs-lookup"><span data-stu-id="65a43-135">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="65a43-136">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="65a43-136">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="65a43-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="65a43-137">-Confirm</span></span>
<span data-ttu-id="65a43-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65a43-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65a43-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65a43-139">-WhatIf</span></span>
<span data-ttu-id="65a43-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65a43-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65a43-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="65a43-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65a43-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65a43-142">CommonParameters</span></span>
<span data-ttu-id="65a43-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65a43-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65a43-144">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="65a43-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65a43-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="65a43-145">INPUTS</span></span>

### <span data-ttu-id="65a43-146">System. String</span><span class="sxs-lookup"><span data-stu-id="65a43-146">System.String</span></span>

## <span data-ttu-id="65a43-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="65a43-147">OUTPUTS</span></span>

### <span data-ttu-id="65a43-148">Microsoft. Azure. Commands. SQL. Server. model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="65a43-148">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="65a43-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="65a43-149">NOTES</span></span>

## <span data-ttu-id="65a43-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="65a43-150">RELATED LINKS</span></span>

[<span data-ttu-id="65a43-151">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="65a43-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
