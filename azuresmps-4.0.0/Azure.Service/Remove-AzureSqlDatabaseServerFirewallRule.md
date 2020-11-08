---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 383DD041-78DC-4170-9529-1FD6F13BC178
online version: ''
schema: 2.0.0
ms.openlocfilehash: 29cbf01629ef772fc41436f3916a2077c1535329
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055072"
---
# <span data-ttu-id="7e40e-101">Remove-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="7e40e-101">Remove-AzureSqlDatabaseServerFirewallRule</span></span>

## <span data-ttu-id="7e40e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7e40e-102">SYNOPSIS</span></span>
<span data-ttu-id="7e40e-103">Usuwa regułę zapory z serwera bazy danych Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="7e40e-103">Removes a firewall rule from an Azure SQL Database server.</span></span>

## <span data-ttu-id="7e40e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7e40e-104">SYNTAX</span></span>

```
Remove-AzureSqlDatabaseServerFirewallRule -ServerName <String> -RuleName <String> [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e40e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7e40e-105">DESCRIPTION</span></span>
<span data-ttu-id="7e40e-106">Polecenie cmdlet **Remove-AzureSqlDatabaseServerFirewallRule** usuwa regułę zapory z wystąpienia serwera bazy danych SQL Azure w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="7e40e-106">The **Remove-AzureSqlDatabaseServerFirewallRule** cmdlet removes a firewall rule from an instance of Azure SQL Database Server in the current subscription.</span></span>

## <span data-ttu-id="7e40e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7e40e-107">EXAMPLES</span></span>

### <span data-ttu-id="7e40e-108">Przykład 1. Usuń regułę</span><span class="sxs-lookup"><span data-stu-id="7e40e-108">Example 1: Remove a rule</span></span>
```
PS C:\>Remove-AzureSqlDatabaseServerFirewallRule -ServerName "lpqd0zbr8y" -RuleName "FirewallRule24"
```

<span data-ttu-id="7e40e-109">To polecenie usuwa regułę zapory o nazwie FirewallRule24 z serwera bazy danych SQL Azure o nazwie lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="7e40e-109">This command removes the firewall rule named FirewallRule24 from the Azure SQL Database server named lpqd0zbr8y.</span></span>

## <span data-ttu-id="7e40e-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7e40e-110">PARAMETERS</span></span>

### <span data-ttu-id="7e40e-111">-Force</span><span class="sxs-lookup"><span data-stu-id="7e40e-111">-Force</span></span>
<span data-ttu-id="7e40e-112">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="7e40e-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e40e-113">-Profile</span><span class="sxs-lookup"><span data-stu-id="7e40e-113">-Profile</span></span>
<span data-ttu-id="7e40e-114">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7e40e-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7e40e-115">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="7e40e-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7e40e-116">-RuleName</span><span class="sxs-lookup"><span data-stu-id="7e40e-116">-RuleName</span></span>
<span data-ttu-id="7e40e-117">Określa nazwę reguły zapory, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7e40e-117">Specifies the name of the firewall rule that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e40e-118">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="7e40e-118">-ServerName</span></span>
<span data-ttu-id="7e40e-119">Określa nazwę serwera.</span><span class="sxs-lookup"><span data-stu-id="7e40e-119">Specifies the name of a server.</span></span>
<span data-ttu-id="7e40e-120">To polecenie cmdlet usuwa regułę zapory z serwera, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="7e40e-120">This cmdlet removes a firewall rule from the server that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e40e-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7e40e-121">-Confirm</span></span>
<span data-ttu-id="7e40e-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7e40e-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e40e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e40e-123">-WhatIf</span></span>
<span data-ttu-id="7e40e-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7e40e-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e40e-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7e40e-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e40e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e40e-126">CommonParameters</span></span>
<span data-ttu-id="7e40e-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e40e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e40e-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e40e-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e40e-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7e40e-129">INPUTS</span></span>

### <span data-ttu-id="7e40e-130">Microsoft. platformy windowsazure. Commands. SQLDatabase. model. SqlDatabaseServerFirewallRuleContext</span><span class="sxs-lookup"><span data-stu-id="7e40e-130">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerFirewallRuleContext</span></span>

## <span data-ttu-id="7e40e-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7e40e-131">OUTPUTS</span></span>

## <span data-ttu-id="7e40e-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7e40e-132">NOTES</span></span>

## <span data-ttu-id="7e40e-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7e40e-133">RELATED LINKS</span></span>

[<span data-ttu-id="7e40e-134">Baza danych SQL Azure</span><span class="sxs-lookup"><span data-stu-id="7e40e-134">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="7e40e-135">Usuwanie reguły zapory</span><span class="sxs-lookup"><span data-stu-id="7e40e-135">Delete Firewall Rule</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505706.aspx)

[<span data-ttu-id="7e40e-136">Operacje dotyczące baz danych platformy Azure SQL</span><span class="sxs-lookup"><span data-stu-id="7e40e-136">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="7e40e-137">Get-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="7e40e-137">Get-AzureSqlDatabaseServerFirewallRule</span></span>](./Get-AzureSqlDatabaseServerFirewallRule.md)

[<span data-ttu-id="7e40e-138">Nowe — AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="7e40e-138">New-AzureSqlDatabaseServerFirewallRule</span></span>](./New-AzureSqlDatabaseServerFirewallRule.md)

[<span data-ttu-id="7e40e-139">Set-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="7e40e-139">Set-AzureSqlDatabaseServerFirewallRule</span></span>](./Set-AzureSqlDatabaseServerFirewallRule.md)


