---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: B5A2F2A8-5D20-47E4-AFC5-44F687142A08
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4e40d833125725f0ae1baff920a283112db24cdc
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054830"
---
# <span data-ttu-id="ee689-101">Set-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="ee689-101">Set-AzureSqlDatabaseServer</span></span>

## <span data-ttu-id="ee689-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ee689-102">SYNOPSIS</span></span>
<span data-ttu-id="ee689-103">Modyfikuje właściwości serwera bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="ee689-103">Modifies the properties of an Azure SQL Database server.</span></span>

## <span data-ttu-id="ee689-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ee689-104">SYNTAX</span></span>

```
Set-AzureSqlDatabaseServer -ServerName <String> -AdminPassword <String> [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee689-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ee689-105">DESCRIPTION</span></span>
<span data-ttu-id="ee689-106">Polecenie cmdlet **Set-AzureSqlDatabaseServer** modyfikuje właściwości określonego wystąpienia serwera bazy danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="ee689-106">The **Set-AzureSqlDatabaseServer** cmdlet modifies the properties of the specified instance of Azure SQL Database Server.</span></span>
<span data-ttu-id="ee689-107">W bieżącej wersji możesz zaktualizować hasło konta administratora dla serwera.</span><span class="sxs-lookup"><span data-stu-id="ee689-107">In the current release, you can only update the administrator account password for a server.</span></span>

## <span data-ttu-id="ee689-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ee689-108">EXAMPLES</span></span>

### <span data-ttu-id="ee689-109">Przykład 1: Zmienianie hasła dla serwera</span><span class="sxs-lookup"><span data-stu-id="ee689-109">Example 1: Change the password for a server</span></span>
```
PS C:\>Set-AzureSqlDatabaseServer -ServerName "lpqd0zbr8y" -AdminPassword "NewPassword"
```

<span data-ttu-id="ee689-110">To polecenie powoduje zmianę hasła konta administratora dla serwera bazy danych SQL Azure o nazwie lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="ee689-110">This command changes the administrator account password for the Azure SQL Database server named lpqd0zbr8y.</span></span>

## <span data-ttu-id="ee689-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ee689-111">PARAMETERS</span></span>

### <span data-ttu-id="ee689-112">-AdminPassword</span><span class="sxs-lookup"><span data-stu-id="ee689-112">-AdminPassword</span></span>
<span data-ttu-id="ee689-113">Określa hasło konta administratora dla serwera bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="ee689-113">Specifies the administrator account password for the Azure SQL Database server.</span></span>
<span data-ttu-id="ee689-114">Musisz określić silne hasło.</span><span class="sxs-lookup"><span data-stu-id="ee689-114">You must specify a strong password.</span></span>
<span data-ttu-id="ee689-115">Aby uzyskać więcej informacji, zobacz [silne hasła](https://go.microsoft.com/fwlink/p/?LinkId=154152) ( https://go.microsoft.com/fwlink/p/?LinkId=154152) w witrynie Microsoft Developer Network).</span><span class="sxs-lookup"><span data-stu-id="ee689-115">For more information, see [Strong Passwords](https://go.microsoft.com/fwlink/p/?LinkId=154152) (https://go.microsoft.com/fwlink/p/?LinkId=154152) at the Microsoft Developer Network.</span></span>

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

### <span data-ttu-id="ee689-116">-Force</span><span class="sxs-lookup"><span data-stu-id="ee689-116">-Force</span></span>
<span data-ttu-id="ee689-117">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="ee689-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ee689-118">-Profile</span><span class="sxs-lookup"><span data-stu-id="ee689-118">-Profile</span></span>
<span data-ttu-id="ee689-119">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ee689-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ee689-120">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="ee689-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ee689-121">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="ee689-121">-ServerName</span></span>
<span data-ttu-id="ee689-122">Określa nazwę serwera, który jest modyfikowany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ee689-122">Specifies the name of the server that this cmdlet modifies.</span></span>
<span data-ttu-id="ee689-123">Określ nazwę serwera, a nie w pełni kwalifikowaną nazwę DNS.</span><span class="sxs-lookup"><span data-stu-id="ee689-123">Specify the server name, not the fully qualified DNS name.</span></span>

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

### <span data-ttu-id="ee689-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ee689-124">-Confirm</span></span>
<span data-ttu-id="ee689-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ee689-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee689-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee689-126">-WhatIf</span></span>
<span data-ttu-id="ee689-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ee689-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee689-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ee689-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee689-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee689-129">CommonParameters</span></span>
<span data-ttu-id="ee689-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee689-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee689-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee689-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee689-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ee689-132">INPUTS</span></span>

### <span data-ttu-id="ee689-133">Microsoft. platformy windowsazure. Commands. SQLDatabase. model. SqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="ee689-133">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerContext</span></span>

## <span data-ttu-id="ee689-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ee689-134">OUTPUTS</span></span>

## <span data-ttu-id="ee689-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ee689-135">NOTES</span></span>

## <span data-ttu-id="ee689-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ee689-136">RELATED LINKS</span></span>

[<span data-ttu-id="ee689-137">Baza danych SQL Azure</span><span class="sxs-lookup"><span data-stu-id="ee689-137">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="ee689-138">Operacje dotyczące baz danych platformy Azure SQL</span><span class="sxs-lookup"><span data-stu-id="ee689-138">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="ee689-139">Get-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="ee689-139">Get-AzureSqlDatabaseServer</span></span>](./Get-AzureSqlDatabaseServer.md)

[<span data-ttu-id="ee689-140">Nowe — AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="ee689-140">New-AzureSqlDatabaseServer</span></span>](./New-AzureSqlDatabaseServer.md)

[<span data-ttu-id="ee689-141">Remove-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="ee689-141">Remove-AzureSqlDatabaseServer</span></span>](./Remove-AzureSqlDatabaseServer.md)


