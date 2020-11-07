---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/disable-azsqlserveradvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerAdvancedDataSecurity.md
ms.openlocfilehash: 482a620552457993795ba03e2da9367df5efa614
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93894105"
---
# <span data-ttu-id="f1fb0-101">Disable-AzSqlServerAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="f1fb0-101">Disable-AzSqlServerAdvancedDataSecurity</span></span>

## <span data-ttu-id="f1fb0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f1fb0-102">SYNOPSIS</span></span>
<span data-ttu-id="f1fb0-103">Wyłącza zaawansowane zabezpieczenia danych na serwerze.</span><span class="sxs-lookup"><span data-stu-id="f1fb0-103">Disables Advanced Data Security on a server.</span></span>

## <span data-ttu-id="f1fb0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f1fb0-104">SYNTAX</span></span>

```
Disable-AzSqlServerAdvancedDataSecurity [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f1fb0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f1fb0-105">DESCRIPTION</span></span>
<span data-ttu-id="f1fb0-106">Polecenie cmdlet **disable-AzSqlServerAdvancedDataSecurity** wyłącza zaawansowane zabezpieczenia danych na serwerze.</span><span class="sxs-lookup"><span data-stu-id="f1fb0-106">The **Disable-AzSqlServerAdvancedDataSecurity** cmdlet disables Advanced Data Security on a server.</span></span>

## <span data-ttu-id="f1fb0-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f1fb0-107">EXAMPLES</span></span>

### <span data-ttu-id="f1fb0-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f1fb0-108">Example 1</span></span>
### <span data-ttu-id="f1fb0-109">Przykład 1-wyłączanie zaawansowanego bezpieczeństwa danych serwera</span><span class="sxs-lookup"><span data-stu-id="f1fb0-109">Example 1 - Disable server Advanced Data Security</span></span>
```powershell
PS C:\>  Disable-AzSqlServerAdvancedDataSecurity `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : False
```

### <span data-ttu-id="f1fb0-110">Przykład 2 — Wyłączenie zaawansowanego zabezpieczenia danych serwera z zasobu serwera</span><span class="sxs-lookup"><span data-stu-id="f1fb0-110">Example 2 - Disable server Advanced Data Security from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Disable-AzSqlServerAdvancedDataSecurity

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : False
```

## <span data-ttu-id="f1fb0-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f1fb0-111">PARAMETERS</span></span>

### <span data-ttu-id="f1fb0-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1fb0-112">-DefaultProfile</span></span>
<span data-ttu-id="f1fb0-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f1fb0-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1fb0-114">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f1fb0-114">-InputObject</span></span>
<span data-ttu-id="f1fb0-115">Obiekt serwera używany z operacją zaawansowanej zasady zabezpieczeń danych</span><span class="sxs-lookup"><span data-stu-id="f1fb0-115">The server object to use with Advanced Data Security policy operation</span></span>

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

### <span data-ttu-id="f1fb0-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1fb0-116">-ResourceGroupName</span></span>
<span data-ttu-id="f1fb0-117">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f1fb0-117">The name of the resource group.</span></span>

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

### <span data-ttu-id="f1fb0-118">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="f1fb0-118">-ServerName</span></span>
<span data-ttu-id="f1fb0-119">Nazwa serwera bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="f1fb0-119">SQL Database server name.</span></span>

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

### <span data-ttu-id="f1fb0-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f1fb0-120">-Confirm</span></span>
<span data-ttu-id="f1fb0-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f1fb0-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1fb0-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1fb0-122">-WhatIf</span></span>
<span data-ttu-id="f1fb0-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f1fb0-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1fb0-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f1fb0-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1fb0-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1fb0-125">CommonParameters</span></span>
<span data-ttu-id="f1fb0-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1fb0-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1fb0-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f1fb0-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1fb0-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f1fb0-128">INPUTS</span></span>

### <span data-ttu-id="f1fb0-129">Microsoft. Azure. Commands. SQL. Server. model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="f1fb0-129">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="f1fb0-130">System. String</span><span class="sxs-lookup"><span data-stu-id="f1fb0-130">System.String</span></span>

## <span data-ttu-id="f1fb0-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f1fb0-131">OUTPUTS</span></span>

### <span data-ttu-id="f1fb0-132">Microsoft. Azure. Commands. SQL. AdvancedThreatProtection. model. ServerAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="f1fb0-132">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="f1fb0-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f1fb0-133">NOTES</span></span>

## <span data-ttu-id="f1fb0-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f1fb0-134">RELATED LINKS</span></span>
