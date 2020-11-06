---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 692D0B64-95EB-4D36-975F-65674B3B2F8C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerAuditing.md
ms.openlocfilehash: ed77001a8eb2a6c0a7869f5aefbbaa93017ede22
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527202"
---
# <span data-ttu-id="83184-101">Remove-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="83184-101">Remove-AzureRmSqlServerAuditing</span></span>

## <span data-ttu-id="83184-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="83184-102">SYNOPSIS</span></span>
<span data-ttu-id="83184-103">Usuwa inspekcję programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="83184-103">Removes the auditing of a SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="83184-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="83184-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerAuditing [-PassThru] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83184-105">Opis</span><span class="sxs-lookup"><span data-stu-id="83184-105">DESCRIPTION</span></span>
<span data-ttu-id="83184-106">Polecenie cmdlet **Remove-AzureRmSqlServerAuditing** umożliwia usunięcie inspekcji programu Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="83184-106">The **Remove-AzureRmSqlServerAuditing** cmdlet removes the auditing of an Azure SQL server.</span></span>
<span data-ttu-id="83184-107">Aby użyć tego polecenia cmdlet, określ parametry *ResourceGroupName* oraz *nazwa_serwera* identyfikujące serwer.</span><span class="sxs-lookup"><span data-stu-id="83184-107">To use this cmdlet, specify the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>
<span data-ttu-id="83184-108">Po uruchomieniu tego polecenia cmdlet Inspekcja baz danych w usłudze Azure SQL Server nie jest wykonywana.</span><span class="sxs-lookup"><span data-stu-id="83184-108">After you run this cmdlet, auditing of the databases on the Azure SQL server is not performed.</span></span>
<span data-ttu-id="83184-109">Jeśli wykonanie polecenia powiedzie się, a następnie określisz parametr *PassThru* , polecenie cmdlet zwróci obiekt opisujący bieżące zasady inspekcji i identyfikatory programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="83184-109">If the command succeeds, and you specify the *PassThru* parameter, the cmdlet returns an object that describes the current auditing policy and the Azure SQL server identifiers.</span></span>
<span data-ttu-id="83184-110">Identyfikatory serwera obejmują **ResourceGroupName** oraz **nazwa_serwera**.</span><span class="sxs-lookup"><span data-stu-id="83184-110">Server identifiers include the **ResourceGroupName** and **ServerName**.</span></span>

## <span data-ttu-id="83184-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="83184-111">EXAMPLES</span></span>

### <span data-ttu-id="83184-112">Przykład 1: usuwanie inspekcji usługi Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="83184-112">Example 1: Remove the auditing of an Azure SQL server</span></span>
```
PS C:\>Remove-AzureRmSqlDatabaseAuditing -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="83184-113">To polecenie usuwa inspekcję wszystkich baz danych znajdujących się w Server01 w grupie zasób.</span><span class="sxs-lookup"><span data-stu-id="83184-113">This command removes the auditing of all the databases located on Server01 in resource group.</span></span>

## <span data-ttu-id="83184-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="83184-114">PARAMETERS</span></span>

### <span data-ttu-id="83184-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="83184-115">-PassThru</span></span>
<span data-ttu-id="83184-116">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="83184-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="83184-117">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="83184-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="83184-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83184-118">-ResourceGroupName</span></span>
<span data-ttu-id="83184-119">Określa nazwę grupy zasobów, do której jest przypisany Program Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="83184-119">Specifies the name of the resource group to which the Azure SQL server is assigned.</span></span>

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

### <span data-ttu-id="83184-120">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="83184-120">-ServerName</span></span>
<span data-ttu-id="83184-121">Określa nazwę programu Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="83184-121">Specifies the name of the Azure SQL server.</span></span>

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

### <span data-ttu-id="83184-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="83184-122">-Confirm</span></span>
<span data-ttu-id="83184-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="83184-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83184-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83184-124">-WhatIf</span></span>
<span data-ttu-id="83184-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="83184-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83184-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="83184-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83184-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83184-127">-DefaultProfile</span></span>
<span data-ttu-id="83184-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="83184-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="83184-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83184-129">CommonParameters</span></span>
<span data-ttu-id="83184-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83184-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83184-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83184-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83184-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="83184-132">INPUTS</span></span>

### <span data-ttu-id="83184-133">Microsoft. Azure. Commands. SQL. Security. model. ServerAuditingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="83184-133">Microsoft.Azure.Commands.Sql.Security.Model.ServerAuditingPolicyModel</span></span>

## <span data-ttu-id="83184-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="83184-134">OUTPUTS</span></span>

### <span data-ttu-id="83184-135">Microsoft. Azure. Commands. SQL. Security. model. ServerAuditingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="83184-135">Microsoft.Azure.Commands.Sql.Security.Model.ServerAuditingPolicyModel</span></span>

## <span data-ttu-id="83184-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="83184-136">NOTES</span></span>

## <span data-ttu-id="83184-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="83184-137">RELATED LINKS</span></span>

[<span data-ttu-id="83184-138">Get-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="83184-138">Get-AzureRmSqlDatabaseAuditingPolicy</span></span>](./Get-AzureRmSqlDatabaseAuditingPolicy.md)

[<span data-ttu-id="83184-139">Set-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="83184-139">Set-AzureRmSqlDatabaseAuditingPolicy</span></span>](./Set-AzureRmSqlDatabaseAuditingPolicy.md)

[<span data-ttu-id="83184-140">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="83184-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


