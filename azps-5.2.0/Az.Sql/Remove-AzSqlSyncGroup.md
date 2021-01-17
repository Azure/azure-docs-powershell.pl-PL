---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncGroup.md
ms.openlocfilehash: 3a5da7972e70e3ebf9c86df62b2bbc79651e72a5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98331045"
---
# <span data-ttu-id="56495-101">Remove-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="56495-101">Remove-AzSqlSyncGroup</span></span>

## <span data-ttu-id="56495-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="56495-102">SYNOPSIS</span></span>
<span data-ttu-id="56495-103">Usuwa grupę usługi Azure SQL Database Sync.</span><span class="sxs-lookup"><span data-stu-id="56495-103">Removes an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="56495-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="56495-104">SYNTAX</span></span>

```
Remove-AzSqlSyncGroup [-Name] <String> [-Force] [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="56495-105">Opis</span><span class="sxs-lookup"><span data-stu-id="56495-105">DESCRIPTION</span></span>
<span data-ttu-id="56495-106">Polecenie cmdlet **Remove-AzSqlSyncGroup** usuwa grupę synchronizacji bazy danych Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="56495-106">The **Remove-AzSqlSyncGroup** cmdlet removes an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="56495-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="56495-107">EXAMPLES</span></span>

### <span data-ttu-id="56495-108">Przykład 1. Usuń grupę synchronizacji</span><span class="sxs-lookup"><span data-stu-id="56495-108">Example 1: Remove a sync group</span></span>
```
PS C:\>Remove-AzSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -Name "syncGroup01"
```

<span data-ttu-id="56495-109">To polecenie usuwa grupę usługi Azure SQL Database Sync o nazwie syncGroup01.</span><span class="sxs-lookup"><span data-stu-id="56495-109">This command removes the Azure SQL Database Sync Group named syncGroup01.</span></span>

## <span data-ttu-id="56495-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="56495-110">PARAMETERS</span></span>

### <span data-ttu-id="56495-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="56495-111">-DatabaseName</span></span>
<span data-ttu-id="56495-112">Nazwa bazy danych SQL Azure Database.</span><span class="sxs-lookup"><span data-stu-id="56495-112">The name of the Azure SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56495-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56495-113">-DefaultProfile</span></span>
<span data-ttu-id="56495-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="56495-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="56495-115">-Force</span><span class="sxs-lookup"><span data-stu-id="56495-115">-Force</span></span>
<span data-ttu-id="56495-116">Pomiń komunikat potwierdzający wykonanie akcji</span><span class="sxs-lookup"><span data-stu-id="56495-116">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="56495-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="56495-117">-Name</span></span>
<span data-ttu-id="56495-118">Nazwa grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="56495-118">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56495-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="56495-119">-PassThru</span></span>
<span data-ttu-id="56495-120">Określa, czy ma zostać zwrócona usunięta Grupa synchronizacji</span><span class="sxs-lookup"><span data-stu-id="56495-120">Defines Whether return the removed sync group</span></span>

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

### <span data-ttu-id="56495-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56495-121">-ResourceGroupName</span></span>
<span data-ttu-id="56495-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="56495-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="56495-123">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="56495-123">-ServerName</span></span>
<span data-ttu-id="56495-124">Nazwa serwera Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="56495-124">The name of the Azure SQL Server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56495-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="56495-125">-Confirm</span></span>
<span data-ttu-id="56495-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56495-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56495-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56495-127">-WhatIf</span></span>
<span data-ttu-id="56495-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56495-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56495-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="56495-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56495-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56495-130">CommonParameters</span></span>
<span data-ttu-id="56495-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56495-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56495-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="56495-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56495-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="56495-133">INPUTS</span></span>

### <span data-ttu-id="56495-134">System. String</span><span class="sxs-lookup"><span data-stu-id="56495-134">System.String</span></span>

## <span data-ttu-id="56495-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="56495-135">OUTPUTS</span></span>

### <span data-ttu-id="56495-136">Microsoft. Azure. Commands. SQL. DataSync. model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="56495-136">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="56495-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="56495-137">NOTES</span></span>

## <span data-ttu-id="56495-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="56495-138">RELATED LINKS</span></span>

[<span data-ttu-id="56495-139">Nowe — AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="56495-139">New-AzSqlSyncGroup</span></span>](./New-AzSqlSyncGroup.md)

[<span data-ttu-id="56495-140">Update-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="56495-140">Update-AzSqlSyncGroup</span></span>](./Update-AzSqlSyncGroup.md)

[<span data-ttu-id="56495-141">Get-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="56495-141">Get-AzSqlSyncGroup</span></span>](./Get-AzSqlSyncGroup.md)

