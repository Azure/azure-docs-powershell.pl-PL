---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: FAAF458C-1662-4130-9A16-0514B714D11D
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServer.md
ms.openlocfilehash: 24249be1d2b5b203a207d72ebd29ec691a90c39a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93887218"
---
# <span data-ttu-id="fd637-101">Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="fd637-101">Set-AzSqlServer</span></span>

## <span data-ttu-id="fd637-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fd637-102">SYNOPSIS</span></span>
<span data-ttu-id="fd637-103">Modyfikuje właściwości serwera bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="fd637-103">Modifies properties of a SQL Database server.</span></span>

## <span data-ttu-id="fd637-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fd637-104">SYNTAX</span></span>

```
Set-AzSqlServer [-ServerName] <String> [-SqlAdministratorPassword <SecureString>] [-Tags <Hashtable>]
 [-ServerVersion <String>] [-AssignIdentity] [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd637-105">Opis</span><span class="sxs-lookup"><span data-stu-id="fd637-105">DESCRIPTION</span></span>
<span data-ttu-id="fd637-106">Polecenie cmdlet **Set-AzSqlServer** modyfikuje właściwości serwera bazy danych Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="fd637-106">The **Set-AzSqlServer** cmdlet modifies properties of an Azure SQL Database server.</span></span>

## <span data-ttu-id="fd637-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fd637-107">EXAMPLES</span></span>

### <span data-ttu-id="fd637-108">Przykład 1: Resetowanie hasła administratora</span><span class="sxs-lookup"><span data-stu-id="fd637-108">Example 1: Reset the administrator password</span></span>
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

<span data-ttu-id="fd637-109">To polecenie resetuje hasło administratora na serwerze AzureSQL o nazwie Server01.</span><span class="sxs-lookup"><span data-stu-id="fd637-109">This command resets the administrator password on the AzureSQL Server named server01.</span></span>

## <span data-ttu-id="fd637-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fd637-110">PARAMETERS</span></span>

### <span data-ttu-id="fd637-111">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="fd637-111">-AssignIdentity</span></span>
<span data-ttu-id="fd637-112">Wygeneruj i przypisz tożsamość usługi Azure Active Directory dla tego serwera do użytku z usługami zarządzania kluczami, takimi jak Magazyn kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="fd637-112">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="fd637-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd637-113">-DefaultProfile</span></span>
<span data-ttu-id="fd637-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="fd637-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fd637-115">-Force</span><span class="sxs-lookup"><span data-stu-id="fd637-115">-Force</span></span>
<span data-ttu-id="fd637-116">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="fd637-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="fd637-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd637-117">-ResourceGroupName</span></span>
<span data-ttu-id="fd637-118">Określa nazwę grupy zasobów, do której jest przypisany serwer.</span><span class="sxs-lookup"><span data-stu-id="fd637-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="fd637-119">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="fd637-119">-ServerName</span></span>
<span data-ttu-id="fd637-120">Określa nazwę serwera, który jest modyfikowany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd637-120">Specifies the name of the server that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="fd637-121">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="fd637-121">-ServerVersion</span></span>
<span data-ttu-id="fd637-122">Określa wersję, do której to polecenie cmdlet zmieni serwer.</span><span class="sxs-lookup"><span data-stu-id="fd637-122">Specifies the version to which this cmdlet changes the server.</span></span> <span data-ttu-id="fd637-123">Dopuszczalne wartości tego parametru to: 2,0 i 12,0.</span><span class="sxs-lookup"><span data-stu-id="fd637-123">The acceptable values for this parameter are: 2.0 and 12.0.</span></span>

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

### <span data-ttu-id="fd637-124">-SqlAdministratorPassword</span><span class="sxs-lookup"><span data-stu-id="fd637-124">-SqlAdministratorPassword</span></span>
<span data-ttu-id="fd637-125">Określa nowe hasło jako element **SecureString** dla administratora serwera bazy danych.</span><span class="sxs-lookup"><span data-stu-id="fd637-125">Specifies a new password, as a **SecureString** , for the database server administrator.</span></span> <span data-ttu-id="fd637-126">Aby uzyskać element **SecureString** , użyj polecenia cmdlet Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="fd637-126">To obtain a **SecureString** , use the Get-Credential cmdlet.</span></span> <span data-ttu-id="fd637-127">Aby uzyskać więcej informacji, wpisz tekst `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="fd637-127">For more information, type `Get-Help
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

### <span data-ttu-id="fd637-128">-Tagi</span><span class="sxs-lookup"><span data-stu-id="fd637-128">-Tags</span></span>
<span data-ttu-id="fd637-129">Określa słownik tagów, które to polecenie cmdlet kojarzy z serwerem.</span><span class="sxs-lookup"><span data-stu-id="fd637-129">Specifies a dictionary of tags that this cmdlet associates with the server.</span></span> <span data-ttu-id="fd637-130">Pary klucz-wartość w formie tabeli skrótów ustawione jako znaczniki na serwerze.</span><span class="sxs-lookup"><span data-stu-id="fd637-130">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="fd637-131">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="fd637-131">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="fd637-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fd637-132">-Confirm</span></span>
<span data-ttu-id="fd637-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd637-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd637-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd637-134">-WhatIf</span></span>
<span data-ttu-id="fd637-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd637-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd637-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="fd637-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd637-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd637-137">CommonParameters</span></span>
<span data-ttu-id="fd637-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd637-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd637-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fd637-139">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd637-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fd637-140">INPUTS</span></span>

### <span data-ttu-id="fd637-141">System. String</span><span class="sxs-lookup"><span data-stu-id="fd637-141">System.String</span></span>

## <span data-ttu-id="fd637-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fd637-142">OUTPUTS</span></span>

### <span data-ttu-id="fd637-143">Microsoft. Azure. Commands. SQL. Server. model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="fd637-143">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="fd637-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fd637-144">NOTES</span></span>

## <span data-ttu-id="fd637-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fd637-145">RELATED LINKS</span></span>

[<span data-ttu-id="fd637-146">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="fd637-146">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
