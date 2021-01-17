---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2A74E72B-BD6B-45D7-9C19-B2575C60C43F
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: df3ed9faa96a98b4e94df370bf90161e7baf2b99
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489526"
---
# <span data-ttu-id="2104a-101">Remove-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="2104a-101">Remove-AzSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="2104a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2104a-102">SYNOPSIS</span></span>
<span data-ttu-id="2104a-103">Usuwa konfigurację odzyskiwania systemu serwera bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="2104a-103">Removes a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="2104a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2104a-104">SYNTAX</span></span>

```
Remove-AzSqlServerDisasterRecoveryConfiguration [-VirtualEndpointName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2104a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2104a-105">DESCRIPTION</span></span>
<span data-ttu-id="2104a-106">Polecenie cmdlet **Remove-AzSqlServerDisasterRecoveryConfiguration** usuwa konfigurację odzyskiwania systemu serwera bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="2104a-106">The **Remove-AzSqlServerDisasterRecoveryConfiguration** cmdlet removes a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="2104a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2104a-107">EXAMPLES</span></span>

## <span data-ttu-id="2104a-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2104a-108">PARAMETERS</span></span>

### <span data-ttu-id="2104a-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2104a-109">-DefaultProfile</span></span>
<span data-ttu-id="2104a-110">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="2104a-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2104a-111">-Force</span><span class="sxs-lookup"><span data-stu-id="2104a-111">-Force</span></span>
<span data-ttu-id="2104a-112">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="2104a-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2104a-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2104a-113">-ResourceGroupName</span></span>
<span data-ttu-id="2104a-114">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2104a-114">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="2104a-115">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="2104a-115">-ServerName</span></span>
<span data-ttu-id="2104a-116">Określa nazwę serwera bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="2104a-116">Specifies the name of a SQL database server.</span></span>

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

### <span data-ttu-id="2104a-117">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="2104a-117">-VirtualEndpointName</span></span>
<span data-ttu-id="2104a-118">Określa nazwę wirtualnego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="2104a-118">Specifies the name of a virtual end point.</span></span>

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

### <span data-ttu-id="2104a-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2104a-119">-Confirm</span></span>
<span data-ttu-id="2104a-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2104a-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2104a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2104a-121">-WhatIf</span></span>
<span data-ttu-id="2104a-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2104a-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2104a-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2104a-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2104a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2104a-124">CommonParameters</span></span>
<span data-ttu-id="2104a-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2104a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2104a-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2104a-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2104a-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2104a-127">INPUTS</span></span>

### <span data-ttu-id="2104a-128">System. String</span><span class="sxs-lookup"><span data-stu-id="2104a-128">System.String</span></span>

## <span data-ttu-id="2104a-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2104a-129">OUTPUTS</span></span>

### <span data-ttu-id="2104a-130">Microsoft. Azure. Commands. SQL. ServerDisasterRecoveryConfiguration. model. AzureSqlServerDisasterRecoveryConfigurationModel</span><span class="sxs-lookup"><span data-stu-id="2104a-130">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="2104a-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2104a-131">NOTES</span></span>

## <span data-ttu-id="2104a-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2104a-132">RELATED LINKS</span></span>

[<span data-ttu-id="2104a-133">Get-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="2104a-133">Get-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="2104a-134">Nowe — AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="2104a-134">New-AzSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="2104a-135">Set-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="2104a-135">Set-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="2104a-136">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="2104a-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
