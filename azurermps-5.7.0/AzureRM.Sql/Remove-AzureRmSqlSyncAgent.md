---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlsyncagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlSyncAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlSyncAgent.md
ms.openlocfilehash: b357c44afd52dd398631b9b7edfcedb0360cf377
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716814"
---
# <span data-ttu-id="81793-101">Remove-AzureRmSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="81793-101">Remove-AzureRmSqlSyncAgent</span></span>

## <span data-ttu-id="81793-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="81793-102">SYNOPSIS</span></span>
<span data-ttu-id="81793-103">Usuwa agenta synchronizacji usługi Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="81793-103">Removes an Azure SQL Sync Agent.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="81793-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="81793-104">SYNTAX</span></span>

```
Remove-AzureRmSqlSyncAgent [-Name] <String> [-Force] [-PassThru] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="81793-105">Opis</span><span class="sxs-lookup"><span data-stu-id="81793-105">DESCRIPTION</span></span>
<span data-ttu-id="81793-106">Polecenie cmdlet **Remove-AzureRmSqlSyncAgent** usuwa agenta synchronizacji Azure SQL Sync.</span><span class="sxs-lookup"><span data-stu-id="81793-106">The **Remove-AzureRmSqlSyncAgent** cmdlet removes an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="81793-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="81793-107">EXAMPLES</span></span>

### <span data-ttu-id="81793-108">Przykład 1: usuwanie agenta synchronizacji</span><span class="sxs-lookup"><span data-stu-id="81793-108">Example 1: Remove a sync agent</span></span>
```
PS C:\>Remove-AzureRmSqlSyncAgent -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -Name "syncAgent01"
```

<span data-ttu-id="81793-109">To polecenie usuwa agenta synchronizacji SQL Azure o nazwie syncAgent01.</span><span class="sxs-lookup"><span data-stu-id="81793-109">This command removes the Azure SQL Sync Agent named syncAgent01.</span></span>

## <span data-ttu-id="81793-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="81793-110">PARAMETERS</span></span>

### <span data-ttu-id="81793-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81793-111">-DefaultProfile</span></span>
<span data-ttu-id="81793-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="81793-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81793-113">-Force</span><span class="sxs-lookup"><span data-stu-id="81793-113">-Force</span></span>
<span data-ttu-id="81793-114">Pomiń komunikat potwierdzający wykonanie akcji</span><span class="sxs-lookup"><span data-stu-id="81793-114">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="81793-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="81793-115">-Name</span></span>
<span data-ttu-id="81793-116">Nazwa agenta synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="81793-116">The sync agent name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SyncAgentName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81793-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="81793-117">-PassThru</span></span>
<span data-ttu-id="81793-118">Określa, czy zwrócić usuniętego agenta synchronizacji</span><span class="sxs-lookup"><span data-stu-id="81793-118">Defines Whether return the removed sync agent</span></span>

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

### <span data-ttu-id="81793-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81793-119">-ResourceGroupName</span></span>
<span data-ttu-id="81793-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="81793-120">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81793-121">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="81793-121">-ServerName</span></span>
<span data-ttu-id="81793-122">Nazwa programu Azure SQL Server, w którym znajduje się Agent synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="81793-122">The name of the Azure SQL Server the sync agent is in.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81793-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="81793-123">-Confirm</span></span>
<span data-ttu-id="81793-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81793-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81793-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81793-125">-WhatIf</span></span>
<span data-ttu-id="81793-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81793-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81793-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="81793-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81793-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81793-128">CommonParameters</span></span>
<span data-ttu-id="81793-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81793-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81793-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81793-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81793-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="81793-131">INPUTS</span></span>

### <span data-ttu-id="81793-132">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="81793-132">None</span></span>
<span data-ttu-id="81793-133">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="81793-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="81793-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="81793-134">OUTPUTS</span></span>

### <span data-ttu-id="81793-135">Microsoft. Azure. Commands. SQL. DataSync. model. AzureSqlSyncAgentModel</span><span class="sxs-lookup"><span data-stu-id="81793-135">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span></span>

## <span data-ttu-id="81793-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="81793-136">NOTES</span></span>

## <span data-ttu-id="81793-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="81793-137">RELATED LINKS</span></span>

[<span data-ttu-id="81793-138">Nowe — AzureRmSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="81793-138">New-AzureRmSqlSyncAgent</span></span>](./New-AzureRmSqlSyncAgent.md)

[<span data-ttu-id="81793-139">Get-AzureRmSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="81793-139">Get-AzureRmSqlSyncAgent</span></span>](./Get-AzureRmSqlSyncAgent.md)

