---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: A723D12D-DCF5-4F0C-AAC2-8BADFBAC3328
online version: ''
schema: 2.0.0
ms.openlocfilehash: a0383e451d8346d4b6465390cc78850b270f6ac3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054935"
---
# <span data-ttu-id="da11d-101">New-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="da11d-101">New-AzureSqlDatabaseServerFirewallRule</span></span>

## <span data-ttu-id="da11d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="da11d-102">SYNOPSIS</span></span>
<span data-ttu-id="da11d-103">Tworzy regułę zapory na serwerze bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="da11d-103">Creates a firewall rule in Azure SQL Database Server.</span></span>

## <span data-ttu-id="da11d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="da11d-104">SYNTAX</span></span>

### <span data-ttu-id="da11d-105">IpRange (domyślny)</span><span class="sxs-lookup"><span data-stu-id="da11d-105">IpRange (Default)</span></span>
```
New-AzureSqlDatabaseServerFirewallRule -ServerName <String> -RuleName <String> -StartIpAddress <String>
 -EndIpAddress <String> [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da11d-106">AllowAllAzureServices</span><span class="sxs-lookup"><span data-stu-id="da11d-106">AllowAllAzureServices</span></span>
```
New-AzureSqlDatabaseServerFirewallRule -ServerName <String> [-RuleName <String>] [-AllowAllAzureServices]
 [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da11d-107">Opis</span><span class="sxs-lookup"><span data-stu-id="da11d-107">DESCRIPTION</span></span>
<span data-ttu-id="da11d-108">Polecenie cmdlet **New-AzureSqlDatabaseServerFirewallRule** powoduje utworzenie reguły zapory w określonym wystąpieniu serwera bazy danych SQL Azure w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="da11d-108">The **New-AzureSqlDatabaseServerFirewallRule** cmdlet creates a firewall rule in the specified instance of Azure SQL Database Server in the current subscription.</span></span>

<span data-ttu-id="da11d-109">Parametry *StartIpAddress* i *EndIpAddress* służą do określenia zakresu adresów IP, które ta reguła zezwala na łączenie się z serwerem bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="da11d-109">Use the *StartIpAddress* and *EndIpAddress* parameters to specify a range of IP addresses that this rule allows to connect to the Azure SQL Database server.</span></span>

<span data-ttu-id="da11d-110">Określ parametr *AllowAllAzureServices* , aby utworzyć regułę umożliwiającą nawiązywanie połączeń platformy Azure z serwerem.</span><span class="sxs-lookup"><span data-stu-id="da11d-110">Specify the *AllowAllAzureServices* parameter to create a rule that allows Azure connections to the server.</span></span>
<span data-ttu-id="da11d-111">Reguła ma początkowe i końcowe wartości adresów IP 0.0.0.0.</span><span class="sxs-lookup"><span data-stu-id="da11d-111">The rule has starting and ending IP address values of 0.0.0.0.</span></span>
<span data-ttu-id="da11d-112">Jeśli nie określisz nazwy reguły zapory, to polecenie cmdlet przypisze domyślną nazwę AllowAllAzureServices.</span><span class="sxs-lookup"><span data-stu-id="da11d-112">If you do not specify a firewall rule name, this cmdlet assigns the default name AllowAllAzureServices.</span></span>

## <span data-ttu-id="da11d-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="da11d-113">EXAMPLES</span></span>

### <span data-ttu-id="da11d-114">Przykład 1. Tworzenie reguły zapory</span><span class="sxs-lookup"><span data-stu-id="da11d-114">Example 1: Create a firewall rule</span></span>
```
PS C:\>New-AzureSqlDatabaseServerFirewallRule -ServerName "lpqd0zbr8y" -RuleName "FirewallRule24" -StartIpAddress 10.1.1.1 -EndIpAddress 10.1.1.2
```

<span data-ttu-id="da11d-115">To polecenie tworzy regułę zapory FirewallRule24 na serwerze bazy danych SQL Azure o nazwie lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="da11d-115">This command creates a firewall rule FirewallRule24 on the Azure SQL Database server named lpqd0zbr8y.</span></span>
<span data-ttu-id="da11d-116">Polecenie określa zakres adresów IP.</span><span class="sxs-lookup"><span data-stu-id="da11d-116">The command specifies an IP address range.</span></span>

### <span data-ttu-id="da11d-117">Przykład 2: Tworzenie reguły umożliwiającej korzystanie ze wszystkich usług platformy Azure</span><span class="sxs-lookup"><span data-stu-id="da11d-117">Example 2: Create a rule that allows all Azure services</span></span>
```
PS C:\>New-AzureSqlDatabaseServerFirewallRule -ServerName "lpqd0zbr8y" -AllowAllAzureServices -RuleName "AzureConnections"
```

<span data-ttu-id="da11d-118">To polecenie tworzy regułę zapory o nazwie AzureConnections na serwerze o nazwie lpqd0zbr8y, który umożliwia nawiązywanie połączeń platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="da11d-118">This command creates a firewall rule named AzureConnections on the server named lpqd0zbr8y that allows Azure connections.</span></span>

### <span data-ttu-id="da11d-119">Przykład 3: Tworzenie reguły pozwalającej wszystkim usługom platformy Azure używającym domyślnej nazwy utworzyć regułę umożliwiającą wszystkim usługom Azure używającym domyślnej nazwy</span><span class="sxs-lookup"><span data-stu-id="da11d-119">Example 3: Create a rule that allows all Azure services that uses the default name Create a rule that allows all Azure services that uses the default name</span></span>
```
PS C:\>New-AzureSqlDatabaseServerFirewallRule -ServerName "lpqd0zbr8y" -AllowAllAzureServices
```

<span data-ttu-id="da11d-120">To polecenie tworzy regułę zapory na określonym serwerze o nazwie lpqd0zbr8y, który umożliwia nawiązywanie połączeń platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="da11d-120">This command creates a firewall rule on the specified server named lpqd0zbr8y that allows Azure connections.</span></span>
<span data-ttu-id="da11d-121">Polecenie przypisuje domyślną nazwę reguły AllowAllAzureServices.</span><span class="sxs-lookup"><span data-stu-id="da11d-121">The command assigns the default rule name AllowAllAzureServices.</span></span>

## <span data-ttu-id="da11d-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="da11d-122">PARAMETERS</span></span>

### <span data-ttu-id="da11d-123">-AllowAllAzureServices</span><span class="sxs-lookup"><span data-stu-id="da11d-123">-AllowAllAzureServices</span></span>
<span data-ttu-id="da11d-124">Wskazuje, że ta reguła zapory umożliwia dostęp do serwera wszystkim adresom IP platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="da11d-124">Indicates that this firewall rule enables all Azure IP addresses to access the server.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AllowAllAzureServices
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da11d-125">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="da11d-125">-EndIpAddress</span></span>
<span data-ttu-id="da11d-126">Określa wartość końcową zakresu adresów IP dla tej reguły.</span><span class="sxs-lookup"><span data-stu-id="da11d-126">Specifies the end value of the IP address range for this rule.</span></span>

```yaml
Type: String
Parameter Sets: IpRange
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da11d-127">-Force</span><span class="sxs-lookup"><span data-stu-id="da11d-127">-Force</span></span>
<span data-ttu-id="da11d-128">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="da11d-128">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="da11d-129">-Profile</span><span class="sxs-lookup"><span data-stu-id="da11d-129">-Profile</span></span>
<span data-ttu-id="da11d-130">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da11d-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="da11d-131">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="da11d-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="da11d-132">-RuleName</span><span class="sxs-lookup"><span data-stu-id="da11d-132">-RuleName</span></span>
<span data-ttu-id="da11d-133">Określa nazwę nowej reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="da11d-133">Specifies the name of the new firewall rule.</span></span>

```yaml
Type: String
Parameter Sets: IpRange
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: AllowAllAzureServices
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da11d-134">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="da11d-134">-ServerName</span></span>
<span data-ttu-id="da11d-135">Określa nazwę serwera.</span><span class="sxs-lookup"><span data-stu-id="da11d-135">Specifies the name of a server.</span></span>
<span data-ttu-id="da11d-136">To polecenie cmdlet powoduje utworzenie reguły zapory na serwerze, który określi to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da11d-136">This cmdlet creates a firewall rule on the server that this cmdlet specifies.</span></span>
<span data-ttu-id="da11d-137">Określ nazwę serwera, a nie w pełni kwalifikowaną nazwę DNS.</span><span class="sxs-lookup"><span data-stu-id="da11d-137">Specify the server name, not the fully qualified DNS name.</span></span>

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

### <span data-ttu-id="da11d-138">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="da11d-138">-StartIpAddress</span></span>
<span data-ttu-id="da11d-139">Określa wartość początkową zakresu adresów IP dla reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="da11d-139">Specifies the start value of the IP address range for the firewall rule.</span></span>

```yaml
Type: String
Parameter Sets: IpRange
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da11d-140">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="da11d-140">-Confirm</span></span>
<span data-ttu-id="da11d-141">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da11d-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da11d-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da11d-142">-WhatIf</span></span>
<span data-ttu-id="da11d-143">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da11d-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da11d-144">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="da11d-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da11d-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da11d-145">CommonParameters</span></span>
<span data-ttu-id="da11d-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da11d-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da11d-147">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da11d-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da11d-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="da11d-148">INPUTS</span></span>

## <span data-ttu-id="da11d-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="da11d-149">OUTPUTS</span></span>

### <span data-ttu-id="da11d-150">Microsoft. platformy windowsazure. Commands. SQLDatabase. model. SqlDatabaseServerFirewallRuleContext</span><span class="sxs-lookup"><span data-stu-id="da11d-150">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerFirewallRuleContext</span></span>

## <span data-ttu-id="da11d-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="da11d-151">NOTES</span></span>

## <span data-ttu-id="da11d-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="da11d-152">RELATED LINKS</span></span>

[<span data-ttu-id="da11d-153">Baza danych SQL Azure</span><span class="sxs-lookup"><span data-stu-id="da11d-153">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="da11d-154">Tworzenie reguły zapory</span><span class="sxs-lookup"><span data-stu-id="da11d-154">Create Firewall Rule</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505712.aspx)

[<span data-ttu-id="da11d-155">Operacje dotyczące baz danych platformy Azure SQL</span><span class="sxs-lookup"><span data-stu-id="da11d-155">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="da11d-156">Get-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="da11d-156">Get-AzureSqlDatabaseServerFirewallRule</span></span>](./Get-AzureSqlDatabaseServerFirewallRule.md)

[<span data-ttu-id="da11d-157">Remove-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="da11d-157">Remove-AzureSqlDatabaseServerFirewallRule</span></span>](./Remove-AzureSqlDatabaseServerFirewallRule.md)

[<span data-ttu-id="da11d-158">Set-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="da11d-158">Set-AzureSqlDatabaseServerFirewallRule</span></span>](./Set-AzureSqlDatabaseServerFirewallRule.md)


