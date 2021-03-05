---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 41D63CC1-5E9F-48D3-89DE-0F753C7475F2
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlserverdisasterrecoveryconfigurationactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDisasterRecoveryConfigurationActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDisasterRecoveryConfigurationActivity.md
ms.openlocfilehash: 68e81a7f51ca385d5671698ad8624f523ae98c53
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962625"
---
# <span data-ttu-id="e9a3e-101">Get-AzSqlServerDisasterRecoveryConfigurationActivity</span><span class="sxs-lookup"><span data-stu-id="e9a3e-101">Get-AzSqlServerDisasterRecoveryConfigurationActivity</span></span>

## <span data-ttu-id="e9a3e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9a3e-102">SYNOPSIS</span></span>
<span data-ttu-id="e9a3e-103">Pobiera aktywność w przypadku konfiguracji odzyskiwania systemu serwera bazy danych.</span><span class="sxs-lookup"><span data-stu-id="e9a3e-103">Gets activity for a database server system recovery configuration.</span></span>

## <span data-ttu-id="e9a3e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e9a3e-104">SYNTAX</span></span>

```
Get-AzSqlServerDisasterRecoveryConfigurationActivity [-ServerName] <String>
 -ServerDisasterRecoveryConfigurationName <String> [-OperationId <Guid>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e9a3e-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="e9a3e-105">DESCRIPTION</span></span>
<span data-ttu-id="e9a3e-106">Polecenie **cmdlet Get-AzSqlServerDisasterRecoveryConfigurationActivity** pobiera aktywność dla konfiguracji odzyskiwania systemu serwera bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="e9a3e-106">The **Get-AzSqlServerDisasterRecoveryConfigurationActivity** cmdlet gets activity for a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="e9a3e-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e9a3e-107">EXAMPLES</span></span>

## <span data-ttu-id="e9a3e-108">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e9a3e-108">PARAMETERS</span></span>

### <span data-ttu-id="e9a3e-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9a3e-109">-DefaultProfile</span></span>
<span data-ttu-id="e9a3e-110">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="e9a3e-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e9a3e-111">-OperationId</span><span class="sxs-lookup"><span data-stu-id="e9a3e-111">-OperationId</span></span>
<span data-ttu-id="e9a3e-112">Określa identyfikator operacji.</span><span class="sxs-lookup"><span data-stu-id="e9a3e-112">Specifies the operation ID.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9a3e-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9a3e-113">-ResourceGroupName</span></span>
<span data-ttu-id="e9a3e-114">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e9a3e-114">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="e9a3e-115">-ServerDisasterRecoveryConfigurationName</span><span class="sxs-lookup"><span data-stu-id="e9a3e-115">-ServerDisasterRecoveryConfigurationName</span></span>
<span data-ttu-id="e9a3e-116">Określa nazwę konfiguracji odzyskiwania systemu serwera.</span><span class="sxs-lookup"><span data-stu-id="e9a3e-116">Specifies the name of the server system recovery configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9a3e-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e9a3e-117">-ServerName</span></span>
<span data-ttu-id="e9a3e-118">Określa nazwę serwera.</span><span class="sxs-lookup"><span data-stu-id="e9a3e-118">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="e9a3e-119">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e9a3e-119">-Confirm</span></span>
<span data-ttu-id="e9a3e-120">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e9a3e-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9a3e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9a3e-121">-WhatIf</span></span>
<span data-ttu-id="e9a3e-122">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e9a3e-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9a3e-123">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e9a3e-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9a3e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9a3e-124">CommonParameters</span></span>
<span data-ttu-id="e9a3e-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9a3e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9a3e-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e9a3e-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9a3e-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e9a3e-127">INPUTS</span></span>

### <span data-ttu-id="e9a3e-128">System.String</span><span class="sxs-lookup"><span data-stu-id="e9a3e-128">System.String</span></span>

### <span data-ttu-id="e9a3e-129">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="e9a3e-129">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="e9a3e-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e9a3e-130">OUTPUTS</span></span>

### <span data-ttu-id="e9a3e-131">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationActivityModel</span><span class="sxs-lookup"><span data-stu-id="e9a3e-131">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationActivityModel</span></span>

## <span data-ttu-id="e9a3e-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e9a3e-132">NOTES</span></span>

## <span data-ttu-id="e9a3e-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e9a3e-133">RELATED LINKS</span></span>

[<span data-ttu-id="e9a3e-134">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="e9a3e-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
