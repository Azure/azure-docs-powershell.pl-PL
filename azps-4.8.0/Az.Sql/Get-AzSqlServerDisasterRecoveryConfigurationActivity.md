---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 41D63CC1-5E9F-48D3-89DE-0F753C7475F2
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverdisasterrecoveryconfigurationactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDisasterRecoveryConfigurationActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDisasterRecoveryConfigurationActivity.md
ms.openlocfilehash: ad3c257366513a5cc9998b4e4edea8879dc38545
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94219788"
---
# <span data-ttu-id="26796-101">Get-AzSqlServerDisasterRecoveryConfigurationActivity</span><span class="sxs-lookup"><span data-stu-id="26796-101">Get-AzSqlServerDisasterRecoveryConfigurationActivity</span></span>

## <span data-ttu-id="26796-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="26796-102">SYNOPSIS</span></span>
<span data-ttu-id="26796-103">Pobiera aktywność dotyczącą konfiguracji odzyskiwania systemu serwera bazy danych.</span><span class="sxs-lookup"><span data-stu-id="26796-103">Gets activity for a database server system recovery configuration.</span></span>

## <span data-ttu-id="26796-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="26796-104">SYNTAX</span></span>

```
Get-AzSqlServerDisasterRecoveryConfigurationActivity [-ServerName] <String>
 -ServerDisasterRecoveryConfigurationName <String> [-OperationId <Guid>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26796-105">Opis</span><span class="sxs-lookup"><span data-stu-id="26796-105">DESCRIPTION</span></span>
<span data-ttu-id="26796-106">Polecenie cmdlet **Get-AzSqlServerDisasterRecoveryConfigurationActivity** pobiera działanie konfiguracji odzyskiwania systemu serwera bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="26796-106">The **Get-AzSqlServerDisasterRecoveryConfigurationActivity** cmdlet gets activity for a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="26796-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="26796-107">EXAMPLES</span></span>

## <span data-ttu-id="26796-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="26796-108">PARAMETERS</span></span>

### <span data-ttu-id="26796-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26796-109">-DefaultProfile</span></span>
<span data-ttu-id="26796-110">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="26796-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="26796-111">-OperationId</span><span class="sxs-lookup"><span data-stu-id="26796-111">-OperationId</span></span>
<span data-ttu-id="26796-112">Określa identyfikator operacji.</span><span class="sxs-lookup"><span data-stu-id="26796-112">Specifies the operation ID.</span></span>

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

### <span data-ttu-id="26796-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26796-113">-ResourceGroupName</span></span>
<span data-ttu-id="26796-114">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="26796-114">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="26796-115">-ServerDisasterRecoveryConfigurationName</span><span class="sxs-lookup"><span data-stu-id="26796-115">-ServerDisasterRecoveryConfigurationName</span></span>
<span data-ttu-id="26796-116">Określa nazwę konfiguracji odzyskiwania systemu serwera.</span><span class="sxs-lookup"><span data-stu-id="26796-116">Specifies the name of the server system recovery configuration.</span></span>

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

### <span data-ttu-id="26796-117">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="26796-117">-ServerName</span></span>
<span data-ttu-id="26796-118">Określa nazwę serwera.</span><span class="sxs-lookup"><span data-stu-id="26796-118">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="26796-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="26796-119">-Confirm</span></span>
<span data-ttu-id="26796-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26796-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26796-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26796-121">-WhatIf</span></span>
<span data-ttu-id="26796-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26796-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26796-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="26796-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26796-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26796-124">CommonParameters</span></span>
<span data-ttu-id="26796-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26796-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26796-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="26796-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26796-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="26796-127">INPUTS</span></span>

### <span data-ttu-id="26796-128">System. String</span><span class="sxs-lookup"><span data-stu-id="26796-128">System.String</span></span>

### <span data-ttu-id="26796-129">System. Nullable "1 [[System. GUID, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="26796-129">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="26796-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="26796-130">OUTPUTS</span></span>

### <span data-ttu-id="26796-131">Microsoft. Azure. Commands. SQL. ServerDisasterRecoveryConfiguration. model. AzureSqlServerDisasterRecoveryConfigurationActivityModel</span><span class="sxs-lookup"><span data-stu-id="26796-131">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationActivityModel</span></span>

## <span data-ttu-id="26796-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="26796-132">NOTES</span></span>

## <span data-ttu-id="26796-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="26796-133">RELATED LINKS</span></span>

[<span data-ttu-id="26796-134">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="26796-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
