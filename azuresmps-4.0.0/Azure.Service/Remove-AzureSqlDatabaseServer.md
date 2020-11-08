---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: F73A078E-F9F2-4520-BF55-DFFE82BE4466
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7a8127a77ecfdc5aa36659060cb5469206a9988d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055073"
---
# <span data-ttu-id="e0e44-101">Remove-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="e0e44-101">Remove-AzureSqlDatabaseServer</span></span>

## <span data-ttu-id="e0e44-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e0e44-102">SYNOPSIS</span></span>
<span data-ttu-id="e0e44-103">Usuwa serwer bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="e0e44-103">Removes an Azure SQL Database server.</span></span>

## <span data-ttu-id="e0e44-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e0e44-104">SYNTAX</span></span>

```
Remove-AzureSqlDatabaseServer -ServerName <String> [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e0e44-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e0e44-105">DESCRIPTION</span></span>
<span data-ttu-id="e0e44-106">Polecenie cmdlet **Remove-AzureSqlDatabaseServer** usuwa określone wystąpienie serwera bazy danych SQL Azure z bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="e0e44-106">The **Remove-AzureSqlDatabaseServer** cmdlet removes the specified instance of Azure SQL Database Server from the current subscription.</span></span>
<span data-ttu-id="e0e44-107">To polecenie cmdlet usuwa wszystkie bazy danych na serwerze.</span><span class="sxs-lookup"><span data-stu-id="e0e44-107">This cmdlet deletes all databases on the server.</span></span>

## <span data-ttu-id="e0e44-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e0e44-108">EXAMPLES</span></span>

### <span data-ttu-id="e0e44-109">Przykład 1: Usuwanie serwera bazy danych</span><span class="sxs-lookup"><span data-stu-id="e0e44-109">Example 1: Remove a database server</span></span>
```
PS C:\>Remove-AzureSqlDatabaseServer -ServerName "lpqd0zbr8y"
```

<span data-ttu-id="e0e44-110">To polecenie usuwa serwer bazy danych SQL Azure o nazwie lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="e0e44-110">This command removes the Azure SQL Database server named lpqd0zbr8y.</span></span>

## <span data-ttu-id="e0e44-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e0e44-111">PARAMETERS</span></span>

### <span data-ttu-id="e0e44-112">-Force</span><span class="sxs-lookup"><span data-stu-id="e0e44-112">-Force</span></span>
<span data-ttu-id="e0e44-113">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="e0e44-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e0e44-114">-Profile</span><span class="sxs-lookup"><span data-stu-id="e0e44-114">-Profile</span></span>
<span data-ttu-id="e0e44-115">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0e44-115">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e0e44-116">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="e0e44-116">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e0e44-117">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="e0e44-117">-ServerName</span></span>
<span data-ttu-id="e0e44-118">Określa nazwę serwera, który jest usuwany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0e44-118">Specifies the name of the server that this cmdlet removes.</span></span>
<span data-ttu-id="e0e44-119">Określ nazwę serwera, a nie w pełni kwalifikowaną nazwę DNS.</span><span class="sxs-lookup"><span data-stu-id="e0e44-119">Specify the server name, not the fully qualified DNS name.</span></span>

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

### <span data-ttu-id="e0e44-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e0e44-120">-Confirm</span></span>
<span data-ttu-id="e0e44-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0e44-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0e44-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0e44-122">-WhatIf</span></span>
<span data-ttu-id="e0e44-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0e44-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0e44-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e0e44-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0e44-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0e44-125">CommonParameters</span></span>
<span data-ttu-id="e0e44-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0e44-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0e44-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0e44-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0e44-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e0e44-128">INPUTS</span></span>

### <span data-ttu-id="e0e44-129">Microsoft. platformy windowsazure. Commands. SQLDatabase. model. SqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="e0e44-129">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerContext</span></span>

## <span data-ttu-id="e0e44-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e0e44-130">OUTPUTS</span></span>

## <span data-ttu-id="e0e44-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e0e44-131">NOTES</span></span>

## <span data-ttu-id="e0e44-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e0e44-132">RELATED LINKS</span></span>

[<span data-ttu-id="e0e44-133">Baza danych SQL Azure</span><span class="sxs-lookup"><span data-stu-id="e0e44-133">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="e0e44-134">Usuwanie serwera</span><span class="sxs-lookup"><span data-stu-id="e0e44-134">Delete Server</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505695.aspx)

[<span data-ttu-id="e0e44-135">Operacje dotyczące baz danych platformy Azure SQL</span><span class="sxs-lookup"><span data-stu-id="e0e44-135">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="e0e44-136">Get-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="e0e44-136">Get-AzureSqlDatabaseServer</span></span>](./Get-AzureSqlDatabaseServer.md)

[<span data-ttu-id="e0e44-137">Nowe — AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="e0e44-137">New-AzureSqlDatabaseServer</span></span>](./New-AzureSqlDatabaseServer.md)

[<span data-ttu-id="e0e44-138">Set-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="e0e44-138">Set-AzureSqlDatabaseServer</span></span>](./Set-AzureSqlDatabaseServer.md)


