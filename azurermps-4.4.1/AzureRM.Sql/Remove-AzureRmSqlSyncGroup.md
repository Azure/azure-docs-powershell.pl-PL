---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlSyncGroup.md
ms.openlocfilehash: 99892ee748de030a045bd9d0a022051206236198
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719511"
---
# <span data-ttu-id="23a00-101">Remove-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="23a00-101">Remove-AzureRmSqlSyncGroup</span></span>

## <span data-ttu-id="23a00-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="23a00-102">SYNOPSIS</span></span>
<span data-ttu-id="23a00-103">Usuwa grupę usługi Azure SQL Database Sync.</span><span class="sxs-lookup"><span data-stu-id="23a00-103">Removes an Azure SQL Database Sync Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="23a00-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="23a00-104">SYNTAX</span></span>

```
Remove-AzureRmSqlSyncGroup [-Name] <String> [-Force] [-PassThru] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23a00-105">Opis</span><span class="sxs-lookup"><span data-stu-id="23a00-105">DESCRIPTION</span></span>
<span data-ttu-id="23a00-106">Polecenie cmdlet **Remove-AzureRmSqlSyncGroup** usuwa grupę synchronizacji bazy danych Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="23a00-106">The **Remove-AzureRmSqlSyncGroup** cmdlet removes an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="23a00-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="23a00-107">EXAMPLES</span></span>

### <span data-ttu-id="23a00-108">Przykład 1. Usuń grupę synchronizacji</span><span class="sxs-lookup"><span data-stu-id="23a00-108">Example 1: Remove a sync group</span></span>
```
PS C:\>Remove-AzureRmSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -Name "syncGroup01"
```

<span data-ttu-id="23a00-109">To polecenie usuwa grupę usługi Azure SQL Database Sync o nazwie syncGroup01.</span><span class="sxs-lookup"><span data-stu-id="23a00-109">This command removes the Azure SQL Database Sync Group named syncGroup01.</span></span>

## <span data-ttu-id="23a00-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="23a00-110">PARAMETERS</span></span>

### <span data-ttu-id="23a00-111">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="23a00-111">-Confirm</span></span>
<span data-ttu-id="23a00-112">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23a00-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23a00-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="23a00-113">-DatabaseName</span></span>
<span data-ttu-id="23a00-114">Nazwa bazy danych SQL Azure Database.</span><span class="sxs-lookup"><span data-stu-id="23a00-114">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="23a00-115">-Force</span><span class="sxs-lookup"><span data-stu-id="23a00-115">-Force</span></span>
<span data-ttu-id="23a00-116">Pomiń komunikat potwierdzający wykonanie akcji</span><span class="sxs-lookup"><span data-stu-id="23a00-116">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="23a00-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="23a00-117">-Name</span></span>
<span data-ttu-id="23a00-118">Nazwa grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="23a00-118">The sync group name.</span></span>

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

### <span data-ttu-id="23a00-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="23a00-119">-PassThru</span></span>
<span data-ttu-id="23a00-120">Określa, czy ma zostać zwrócona usunięta Grupa synchronizacji</span><span class="sxs-lookup"><span data-stu-id="23a00-120">Defines Whether return the removed sync group</span></span>

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

### <span data-ttu-id="23a00-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23a00-121">-ResourceGroupName</span></span>
<span data-ttu-id="23a00-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="23a00-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="23a00-123">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="23a00-123">-ServerName</span></span>
<span data-ttu-id="23a00-124">Nazwa serwera Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="23a00-124">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="23a00-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23a00-125">-WhatIf</span></span>
<span data-ttu-id="23a00-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23a00-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23a00-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="23a00-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23a00-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23a00-128">-DefaultProfile</span></span>
<span data-ttu-id="23a00-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="23a00-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="23a00-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23a00-130">CommonParameters</span></span>
<span data-ttu-id="23a00-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23a00-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23a00-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23a00-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23a00-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="23a00-133">INPUTS</span></span>

## <span data-ttu-id="23a00-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="23a00-134">OUTPUTS</span></span>

### <span data-ttu-id="23a00-135">Microsoft. Azure. Commands. SQL. DataSync. model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="23a00-135">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="23a00-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="23a00-136">NOTES</span></span>

## <span data-ttu-id="23a00-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="23a00-137">RELATED LINKS</span></span>

[<span data-ttu-id="23a00-138">Nowe — AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="23a00-138">New-AzureRmSqlSyncGroup</span></span>](./New-AzureRmSqlSyncGroup.md)

[<span data-ttu-id="23a00-139">Update-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="23a00-139">Update-AzureRmSqlSyncGroup</span></span>](./Update-AzureRmSqlSyncGroup.md)

[<span data-ttu-id="23a00-140">Get-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="23a00-140">Get-AzureRmSqlSyncGroup</span></span>](./Get-AzureRmSqlSyncGroup.md)

