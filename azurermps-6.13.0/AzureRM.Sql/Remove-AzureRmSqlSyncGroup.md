---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlSyncGroup.md
ms.openlocfilehash: 62f3c74f94ac0e775adc70f4eef9c4250e041145
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553423"
---
# <span data-ttu-id="540a9-101">Remove-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="540a9-101">Remove-AzureRmSqlSyncGroup</span></span>

## <span data-ttu-id="540a9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="540a9-102">SYNOPSIS</span></span>
<span data-ttu-id="540a9-103">Usuwa grupę usługi Azure SQL Database Sync.</span><span class="sxs-lookup"><span data-stu-id="540a9-103">Removes an Azure SQL Database Sync Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="540a9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="540a9-104">SYNTAX</span></span>

```
Remove-AzureRmSqlSyncGroup [-Name] <String> [-Force] [-PassThru] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="540a9-105">Opis</span><span class="sxs-lookup"><span data-stu-id="540a9-105">DESCRIPTION</span></span>
<span data-ttu-id="540a9-106">Polecenie cmdlet **Remove-AzureRmSqlSyncGroup** usuwa grupę synchronizacji bazy danych Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="540a9-106">The **Remove-AzureRmSqlSyncGroup** cmdlet removes an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="540a9-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="540a9-107">EXAMPLES</span></span>

### <span data-ttu-id="540a9-108">Przykład 1. Usuń grupę synchronizacji</span><span class="sxs-lookup"><span data-stu-id="540a9-108">Example 1: Remove a sync group</span></span>
```
PS C:\>Remove-AzureRmSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -Name "syncGroup01"
```

<span data-ttu-id="540a9-109">To polecenie usuwa grupę usługi Azure SQL Database Sync o nazwie syncGroup01.</span><span class="sxs-lookup"><span data-stu-id="540a9-109">This command removes the Azure SQL Database Sync Group named syncGroup01.</span></span>

## <span data-ttu-id="540a9-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="540a9-110">PARAMETERS</span></span>

### <span data-ttu-id="540a9-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="540a9-111">-DatabaseName</span></span>
<span data-ttu-id="540a9-112">Nazwa bazy danych SQL Azure Database.</span><span class="sxs-lookup"><span data-stu-id="540a9-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="540a9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="540a9-113">-DefaultProfile</span></span>
<span data-ttu-id="540a9-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="540a9-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="540a9-115">-Force</span><span class="sxs-lookup"><span data-stu-id="540a9-115">-Force</span></span>
<span data-ttu-id="540a9-116">Pomiń komunikat potwierdzający wykonanie akcji</span><span class="sxs-lookup"><span data-stu-id="540a9-116">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="540a9-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="540a9-117">-Name</span></span>
<span data-ttu-id="540a9-118">Nazwa grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="540a9-118">The sync group name.</span></span>

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

### <span data-ttu-id="540a9-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="540a9-119">-PassThru</span></span>
<span data-ttu-id="540a9-120">Określa, czy ma zostać zwrócona usunięta Grupa synchronizacji</span><span class="sxs-lookup"><span data-stu-id="540a9-120">Defines Whether return the removed sync group</span></span>

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

### <span data-ttu-id="540a9-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="540a9-121">-ResourceGroupName</span></span>
<span data-ttu-id="540a9-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="540a9-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="540a9-123">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="540a9-123">-ServerName</span></span>
<span data-ttu-id="540a9-124">Nazwa serwera Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="540a9-124">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="540a9-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="540a9-125">-Confirm</span></span>
<span data-ttu-id="540a9-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="540a9-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="540a9-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="540a9-127">-WhatIf</span></span>
<span data-ttu-id="540a9-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="540a9-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="540a9-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="540a9-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="540a9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="540a9-130">CommonParameters</span></span>
<span data-ttu-id="540a9-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="540a9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="540a9-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="540a9-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="540a9-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="540a9-133">INPUTS</span></span>

### <span data-ttu-id="540a9-134">System. String</span><span class="sxs-lookup"><span data-stu-id="540a9-134">System.String</span></span>

## <span data-ttu-id="540a9-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="540a9-135">OUTPUTS</span></span>

### <span data-ttu-id="540a9-136">Microsoft. Azure. Commands. SQL. DataSync. model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="540a9-136">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="540a9-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="540a9-137">NOTES</span></span>

## <span data-ttu-id="540a9-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="540a9-138">RELATED LINKS</span></span>

[<span data-ttu-id="540a9-139">Nowe — AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="540a9-139">New-AzureRmSqlSyncGroup</span></span>](./New-AzureRmSqlSyncGroup.md)

[<span data-ttu-id="540a9-140">Update-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="540a9-140">Update-AzureRmSqlSyncGroup</span></span>](./Update-AzureRmSqlSyncGroup.md)

[<span data-ttu-id="540a9-141">Get-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="540a9-141">Get-AzureRmSqlSyncGroup</span></span>](./Get-AzureRmSqlSyncGroup.md)

