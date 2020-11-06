---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Update-AzureRmSqlSyncSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Update-AzureRmSqlSyncSchema.md
ms.openlocfilehash: 34aec11e5f4bd2ee0aef37a4287544081bb9a87a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549087"
---
# <span data-ttu-id="31c9d-101">Update-AzureRmSqlSyncSchema</span><span class="sxs-lookup"><span data-stu-id="31c9d-101">Update-AzureRmSqlSyncSchema</span></span>

## <span data-ttu-id="31c9d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="31c9d-102">SYNOPSIS</span></span>
<span data-ttu-id="31c9d-103">Aktualizowanie schematu synchronizowania bazy danych członka synchronizacji lub bazy danych Centrum synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="31c9d-103">Update the sync schema for a sync member database or a sync hub database.</span></span>
<span data-ttu-id="31c9d-104">Pobierze on najnowszą wersję schematu bazy danych z rzeczywistej bazy danych, a następnie użyje go w celu odświeżenia schematu buforowanego przez bazę danych metadanych synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="31c9d-104">It will get the latest database schema from the real database and then use it refresh the schema cached by Sync metadata database.</span></span>
<span data-ttu-id="31c9d-105">Jeśli zostanie określona wartość "SyncMemberName", spowoduje to odświeżenie schematu bazy danych członka. Jeśli nie, zostanie odświeżony schemat bazy danych centrum.</span><span class="sxs-lookup"><span data-stu-id="31c9d-105">If "SyncMemberName" is specified, it will refresh the member database schema; if not, it will refresh the hub database schema.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="31c9d-106">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="31c9d-106">SYNTAX</span></span>

```
Update-AzureRmSqlSyncSchema [-SyncGroupName] <String> [-SyncMemberName <String>] [-PassThru]
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31c9d-107">Opis</span><span class="sxs-lookup"><span data-stu-id="31c9d-107">DESCRIPTION</span></span>
<span data-ttu-id="31c9d-108">Polecenie cmdlet **Update-AzureRmSqlSyncSchema** aktualizuje schemat synchronizacji dla bazy danych członka synchronizacji lub bazy danych Centrum synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="31c9d-108">The **Update-AzureRmSqlSyncSchema** cmdlet updates the sync schema for a sync member database or a sync hub database.</span></span>

## <span data-ttu-id="31c9d-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="31c9d-109">EXAMPLES</span></span>

### <span data-ttu-id="31c9d-110">Przykład 1: aktualizowanie schematu synchronizacji dla bazy danych centrum</span><span class="sxs-lookup"><span data-stu-id="31c9d-110">Example 1: Update the sync schema for a hub database</span></span>
```
PS C:\>Update-AzureRmSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01"
```

<span data-ttu-id="31c9d-111">To polecenie aktualizuje schemat synchronizacji dla bazy danych centrum w grupie synchronizacja syncGroup01</span><span class="sxs-lookup"><span data-stu-id="31c9d-111">This command updates the sync schema for the hub database in the sync group syncGroup01</span></span>

### <span data-ttu-id="31c9d-112">Przykład 2: aktualizowanie schematu synchronizacji dla bazy danych członka</span><span class="sxs-lookup"><span data-stu-id="31c9d-112">Example 2: Update the sync schema for a member database</span></span>
```
PS C:\>Update-AzureRmSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01" -SyncMemberName "syncMember01"
```

<span data-ttu-id="31c9d-113">To polecenie aktualizuje schemat synchronizacji bazy danych elementu członkowskiego w synchronizacji elementu członkowskiego synchronizacji syncMember01</span><span class="sxs-lookup"><span data-stu-id="31c9d-113">This command updates the sync schema for the member database in the sync member syncMember01</span></span>

## <span data-ttu-id="31c9d-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="31c9d-114">PARAMETERS</span></span>

### <span data-ttu-id="31c9d-115">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="31c9d-115">-Confirm</span></span>
<span data-ttu-id="31c9d-116">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="31c9d-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31c9d-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="31c9d-117">-DatabaseName</span></span>
<span data-ttu-id="31c9d-118">Nazwa bazy danych SQL Azure Database.</span><span class="sxs-lookup"><span data-stu-id="31c9d-118">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="31c9d-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="31c9d-119">-PassThru</span></span>
<span data-ttu-id="31c9d-120">Określa, czy ma być zwracana Grupa synchronizacji, na której działa to polecenie cmdlet</span><span class="sxs-lookup"><span data-stu-id="31c9d-120">Defines Whether return the sync group this cmdlet works on</span></span>

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

### <span data-ttu-id="31c9d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31c9d-121">-ResourceGroupName</span></span>
<span data-ttu-id="31c9d-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="31c9d-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="31c9d-123">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="31c9d-123">-ServerName</span></span>
<span data-ttu-id="31c9d-124">Nazwa serwera Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="31c9d-124">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="31c9d-125">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="31c9d-125">-SyncGroupName</span></span>
<span data-ttu-id="31c9d-126">Nazwa grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="31c9d-126">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31c9d-127">-SyncMemberName</span><span class="sxs-lookup"><span data-stu-id="31c9d-127">-SyncMemberName</span></span>
<span data-ttu-id="31c9d-128">Nazwa członka synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="31c9d-128">The sync member name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31c9d-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31c9d-129">-WhatIf</span></span>
<span data-ttu-id="31c9d-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="31c9d-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="31c9d-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="31c9d-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31c9d-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31c9d-132">-DefaultProfile</span></span>
<span data-ttu-id="31c9d-133">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="31c9d-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="31c9d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31c9d-134">CommonParameters</span></span>
<span data-ttu-id="31c9d-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31c9d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31c9d-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31c9d-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31c9d-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="31c9d-137">INPUTS</span></span>

## <span data-ttu-id="31c9d-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="31c9d-138">OUTPUTS</span></span>

### <span data-ttu-id="31c9d-139">Microsoft. Azure. Commands. SQL. DataSync. model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="31c9d-139">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="31c9d-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="31c9d-140">NOTES</span></span>

## <span data-ttu-id="31c9d-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="31c9d-141">RELATED LINKS</span></span>

