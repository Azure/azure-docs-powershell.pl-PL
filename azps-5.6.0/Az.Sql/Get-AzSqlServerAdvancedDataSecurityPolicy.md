---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlserveradvanceddatasecuritypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedDataSecurityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedDataSecurityPolicy.md
ms.openlocfilehash: 372951b708d34c44706f981424b7ace39efff2b3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974186"
---
# <span data-ttu-id="839a0-101">Get-AzSqlServerAdvancedDataSecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="839a0-101">Get-AzSqlServerAdvancedDataSecurityPolicy</span></span>

## <span data-ttu-id="839a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="839a0-102">SYNOPSIS</span></span>
<span data-ttu-id="839a0-103">Pobiera zaawansowane zasady zabezpieczeń danych serwera.</span><span class="sxs-lookup"><span data-stu-id="839a0-103">Gets Advanced Data Security policy of a server.</span></span>

## <span data-ttu-id="839a0-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="839a0-104">SYNTAX</span></span>

```
Get-AzSqlServerAdvancedDataSecurityPolicy [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="839a0-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="839a0-105">DESCRIPTION</span></span>
<span data-ttu-id="839a0-106">Polecenie **cmdlet Get-AzSqlServerAdvancedDataSecurityPolicy** pobiera zasady advanced data security serwera.</span><span class="sxs-lookup"><span data-stu-id="839a0-106">The **Get-AzSqlServerAdvancedDataSecurityPolicy** cmdlet retrieves the Advanced Data Security policy of a server.</span></span>

## <span data-ttu-id="839a0-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="839a0-107">EXAMPLES</span></span>

### <span data-ttu-id="839a0-108">Przykład 1. Pobiera zaawansowane zabezpieczenia danych serwera</span><span class="sxs-lookup"><span data-stu-id="839a0-108">Example 1: Gets server Advanced Data Security</span></span>
```powershell
PS C:\>  Get-AzSqlServerAdvancedDataSecurityPolicy `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

### <span data-ttu-id="839a0-109">Przykład 2. Pobiera zaawansowane zabezpieczenia danych serwera z zasobu serwera</span><span class="sxs-lookup"><span data-stu-id="839a0-109">Example 2: Gets server Advanced Data Security from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Get-AzSqlServerAdvancedDataSecurityPolicy

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

## <span data-ttu-id="839a0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="839a0-110">PARAMETERS</span></span>

### <span data-ttu-id="839a0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="839a0-111">-DefaultProfile</span></span>
<span data-ttu-id="839a0-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="839a0-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="839a0-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="839a0-113">-InputObject</span></span>
<span data-ttu-id="839a0-114">Obiekt serwera do użycia z operacją zasad zaawansowanego zabezpieczeń danych</span><span class="sxs-lookup"><span data-stu-id="839a0-114">The server object to use with Advanced Data Security policy operation</span></span>

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

### <span data-ttu-id="839a0-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="839a0-115">-ResourceGroupName</span></span>
<span data-ttu-id="839a0-116">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="839a0-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="839a0-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="839a0-117">-ServerName</span></span>
<span data-ttu-id="839a0-118">Nazwa serwera bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="839a0-118">SQL Database server name.</span></span>

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

### <span data-ttu-id="839a0-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="839a0-119">CommonParameters</span></span>
<span data-ttu-id="839a0-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="839a0-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="839a0-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="839a0-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="839a0-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="839a0-122">INPUTS</span></span>

### <span data-ttu-id="839a0-123">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="839a0-123">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="839a0-124">System.String</span><span class="sxs-lookup"><span data-stu-id="839a0-124">System.String</span></span>

## <span data-ttu-id="839a0-125">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="839a0-125">OUTPUTS</span></span>

### <span data-ttu-id="839a0-126">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="839a0-126">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="839a0-127">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="839a0-127">NOTES</span></span>

## <span data-ttu-id="839a0-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="839a0-128">RELATED LINKS</span></span>
