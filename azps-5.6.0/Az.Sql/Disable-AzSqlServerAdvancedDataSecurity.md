---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/disable-azsqlserveradvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerAdvancedDataSecurity.md
ms.openlocfilehash: 4abe17fb272e97637bbd43a69401f9c101f14ef6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967585"
---
# <span data-ttu-id="08f25-101">Disable-AzSqlServerAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="08f25-101">Disable-AzSqlServerAdvancedDataSecurity</span></span>

## <span data-ttu-id="08f25-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="08f25-102">SYNOPSIS</span></span>
<span data-ttu-id="08f25-103">Wyłącza zaawansowane zabezpieczenia danych na serwerze.</span><span class="sxs-lookup"><span data-stu-id="08f25-103">Disables Advanced Data Security on a server.</span></span>

## <span data-ttu-id="08f25-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="08f25-104">SYNTAX</span></span>

```
Disable-AzSqlServerAdvancedDataSecurity [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="08f25-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="08f25-105">DESCRIPTION</span></span>
<span data-ttu-id="08f25-106">Polecenie **cmdlet Disable-AzSqlServerAdvancedDataSecurity** wyłącza zaawansowane zabezpieczenia danych na serwerze.</span><span class="sxs-lookup"><span data-stu-id="08f25-106">The **Disable-AzSqlServerAdvancedDataSecurity** cmdlet disables Advanced Data Security on a server.</span></span>

## <span data-ttu-id="08f25-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="08f25-107">EXAMPLES</span></span>

### <span data-ttu-id="08f25-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="08f25-108">Example 1</span></span>
### <span data-ttu-id="08f25-109">Przykład 2. Wyłączanie zaawansowanych zabezpieczeń danych serwera</span><span class="sxs-lookup"><span data-stu-id="08f25-109">Example 2: Disable server Advanced Data Security</span></span>
```powershell
PS C:\>  Disable-AzSqlServerAdvancedDataSecurity `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : False
```

### <span data-ttu-id="08f25-110">Przykład 3. Wyłączanie zaawansowanych zabezpieczeń danych serwera z zasobu serwera</span><span class="sxs-lookup"><span data-stu-id="08f25-110">Example 3: Disable server Advanced Data Security from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Disable-AzSqlServerAdvancedDataSecurity

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : False
```

## <span data-ttu-id="08f25-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="08f25-111">PARAMETERS</span></span>

### <span data-ttu-id="08f25-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08f25-112">-DefaultProfile</span></span>
<span data-ttu-id="08f25-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="08f25-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="08f25-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="08f25-114">-InputObject</span></span>
<span data-ttu-id="08f25-115">Obiekt serwera do użycia z operacją zasad zaawansowanego zabezpieczeń danych</span><span class="sxs-lookup"><span data-stu-id="08f25-115">The server object to use with Advanced Data Security policy operation</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="08f25-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08f25-116">-ResourceGroupName</span></span>
<span data-ttu-id="08f25-117">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="08f25-117">The name of the resource group.</span></span>

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

### <span data-ttu-id="08f25-118">-ServerName</span><span class="sxs-lookup"><span data-stu-id="08f25-118">-ServerName</span></span>
<span data-ttu-id="08f25-119">Nazwa serwera bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="08f25-119">SQL Database server name.</span></span>

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

### <span data-ttu-id="08f25-120">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="08f25-120">-Confirm</span></span>
<span data-ttu-id="08f25-121">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="08f25-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08f25-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08f25-122">-WhatIf</span></span>
<span data-ttu-id="08f25-123">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="08f25-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08f25-124">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="08f25-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08f25-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08f25-125">CommonParameters</span></span>
<span data-ttu-id="08f25-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08f25-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08f25-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="08f25-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08f25-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="08f25-128">INPUTS</span></span>

### <span data-ttu-id="08f25-129">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="08f25-129">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="08f25-130">System.String</span><span class="sxs-lookup"><span data-stu-id="08f25-130">System.String</span></span>

## <span data-ttu-id="08f25-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="08f25-131">OUTPUTS</span></span>

### <span data-ttu-id="08f25-132">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="08f25-132">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="08f25-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="08f25-133">NOTES</span></span>

## <span data-ttu-id="08f25-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="08f25-134">RELATED LINKS</span></span>
