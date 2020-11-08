---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: F311A7A9-5FE9-4E81-8FF1-8E3A02F2BF4B
online version: ''
schema: 2.0.0
ms.openlocfilehash: ce9d384a5dd7f57fb4444fb173864ec5859b3a81
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054829"
---
# <span data-ttu-id="a300a-101">Set-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="a300a-101">Set-AzureSqlDatabaseServerFirewallRule</span></span>

## <span data-ttu-id="a300a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a300a-102">SYNOPSIS</span></span>
<span data-ttu-id="a300a-103">Modyfikuje istniejącą regułę zapory na serwerze bazy danych Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="a300a-103">Modifies an existing firewall rule in an Azure SQL Database Server.</span></span>

## <span data-ttu-id="a300a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a300a-104">SYNTAX</span></span>

```
Set-AzureSqlDatabaseServerFirewallRule -ServerName <String> -RuleName <String> -StartIpAddress <String>
 -EndIpAddress <String> [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a300a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a300a-105">DESCRIPTION</span></span>
<span data-ttu-id="a300a-106">Polecenie cmdlet **Set-AzureSqlDatabaseServerFirewallRule** modyfikuje wartości początkowy adres IP i końcowy adres IP istniejącej reguły zapory w określonym wystąpieniu serwera bazy danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="a300a-106">The **Set-AzureSqlDatabaseServerFirewallRule** cmdlet modifies the start IP address and end IP address values of an existing firewall rule in the specified instance of Azure SQL Database Server.</span></span>

## <span data-ttu-id="a300a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a300a-107">EXAMPLES</span></span>

### <span data-ttu-id="a300a-108">Przykład 1. Modyfikowanie reguły zapory</span><span class="sxs-lookup"><span data-stu-id="a300a-108">Example 1: Modify a firewall rule</span></span>
```
PS C:\> Set-AzureSqlDatabaseServerFirewallRule -ServerName "lpqd0zbr8y" -RuleName "FirewallRule24" -StartIpAddress 10.1.1.2 -EndIpAddress 10.1.1.4
```

<span data-ttu-id="a300a-109">To polecenie modyfikuje początkowy adres IP i końcowy adres IP reguły zapory o nazwie FirewallRule24 na serwerze bazy danych SQL Azure o nazwie lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="a300a-109">This command modifies the start IP address and end IP address of the firewall rule named FirewallRule24 on the Azure SQL Database server named lpqd0zbr8y.</span></span>

## <span data-ttu-id="a300a-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a300a-110">PARAMETERS</span></span>

### <span data-ttu-id="a300a-111">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="a300a-111">-EndIpAddress</span></span>
<span data-ttu-id="a300a-112">Określa wartość końcową zakresu adresów IP dla tej reguły.</span><span class="sxs-lookup"><span data-stu-id="a300a-112">Specifies the end value of the IP address range for this rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a300a-113">-Force</span><span class="sxs-lookup"><span data-stu-id="a300a-113">-Force</span></span>
<span data-ttu-id="a300a-114">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="a300a-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a300a-115">-Profile</span><span class="sxs-lookup"><span data-stu-id="a300a-115">-Profile</span></span>
<span data-ttu-id="a300a-116">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a300a-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a300a-117">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="a300a-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a300a-118">-RuleName</span><span class="sxs-lookup"><span data-stu-id="a300a-118">-RuleName</span></span>
<span data-ttu-id="a300a-119">Określa nazwę reguły zapory, którą to polecenie cmdlet modyfikuje.</span><span class="sxs-lookup"><span data-stu-id="a300a-119">Specifies the name of the firewall rule that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="a300a-120">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="a300a-120">-ServerName</span></span>
<span data-ttu-id="a300a-121">Określa nazwę serwera.</span><span class="sxs-lookup"><span data-stu-id="a300a-121">Specifies the name of a server.</span></span>
<span data-ttu-id="a300a-122">To polecenie cmdlet powoduje utworzenie reguły zapory na serwerze, który określi to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a300a-122">This cmdlet creates a firewall rule on the server that this cmdlet specifies.</span></span>
<span data-ttu-id="a300a-123">Określ nazwę serwera, a nie w pełni kwalifikowaną nazwę DNS.</span><span class="sxs-lookup"><span data-stu-id="a300a-123">Specify the server name, not the fully qualified DNS name.</span></span>

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

### <span data-ttu-id="a300a-124">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="a300a-124">-StartIpAddress</span></span>
<span data-ttu-id="a300a-125">Określa wartość początkową zakresu adresów IP dla reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="a300a-125">Specifies the start value of the IP address range for the firewall rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a300a-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a300a-126">-Confirm</span></span>
<span data-ttu-id="a300a-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a300a-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a300a-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a300a-128">-WhatIf</span></span>
<span data-ttu-id="a300a-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a300a-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a300a-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a300a-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a300a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a300a-131">CommonParameters</span></span>
<span data-ttu-id="a300a-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a300a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a300a-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a300a-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a300a-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a300a-134">INPUTS</span></span>

### <span data-ttu-id="a300a-135">Microsoft. platformy windowsazure. Commands. SQLDatabase. model. SqlDatabaseServerFirewallRuleContext</span><span class="sxs-lookup"><span data-stu-id="a300a-135">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerFirewallRuleContext</span></span>

## <span data-ttu-id="a300a-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a300a-136">OUTPUTS</span></span>

### <span data-ttu-id="a300a-137">Microsoft. platformy windowsazure. Commands. SQLDatabase. model. SqlDatabaseServerFirewallRuleContext</span><span class="sxs-lookup"><span data-stu-id="a300a-137">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerFirewallRuleContext</span></span>

## <span data-ttu-id="a300a-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a300a-138">NOTES</span></span>

## <span data-ttu-id="a300a-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a300a-139">RELATED LINKS</span></span>

[<span data-ttu-id="a300a-140">Baza danych SQL Azure</span><span class="sxs-lookup"><span data-stu-id="a300a-140">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="a300a-141">Operacje dotyczące baz danych platformy Azure SQL</span><span class="sxs-lookup"><span data-stu-id="a300a-141">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="a300a-142">Ustawianie reguły zapory</span><span class="sxs-lookup"><span data-stu-id="a300a-142">Set Firewall Rule</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505707.aspx)

[<span data-ttu-id="a300a-143">Get-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="a300a-143">Get-AzureSqlDatabaseServerFirewallRule</span></span>](./Get-AzureSqlDatabaseServerFirewallRule.md)

[<span data-ttu-id="a300a-144">Nowe — AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="a300a-144">New-AzureSqlDatabaseServerFirewallRule</span></span>](./New-AzureSqlDatabaseServerFirewallRule.md)

[<span data-ttu-id="a300a-145">Remove-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="a300a-145">Remove-AzureSqlDatabaseServerFirewallRule</span></span>](./Remove-AzureSqlDatabaseServerFirewallRule.md)


