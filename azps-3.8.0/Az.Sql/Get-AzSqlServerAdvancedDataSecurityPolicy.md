---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserveradvanceddatasecuritypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedDataSecurityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedDataSecurityPolicy.md
ms.openlocfilehash: 14075af7cd18b27965de66c738edfaf0ffe64fd3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94052037"
---
# <span data-ttu-id="35a53-101">Get-AzSqlServerAdvancedDataSecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="35a53-101">Get-AzSqlServerAdvancedDataSecurityPolicy</span></span>

## <span data-ttu-id="35a53-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="35a53-102">SYNOPSIS</span></span>
<span data-ttu-id="35a53-103">Pobiera zaawansowane zasady zabezpieczeń danych serwera.</span><span class="sxs-lookup"><span data-stu-id="35a53-103">Gets Advanced Data Security policy of a server.</span></span>

## <span data-ttu-id="35a53-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="35a53-104">SYNTAX</span></span>

```
Get-AzSqlServerAdvancedDataSecurityPolicy [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="35a53-105">Opis</span><span class="sxs-lookup"><span data-stu-id="35a53-105">DESCRIPTION</span></span>
<span data-ttu-id="35a53-106">Polecenie cmdlet **Get-AzSqlServerAdvancedDataSecurityPolicy** pobiera zaawansowane zasady zabezpieczeń danych serwera.</span><span class="sxs-lookup"><span data-stu-id="35a53-106">The **Get-AzSqlServerAdvancedDataSecurityPolicy** cmdlet retrieves the Advanced Data Security policy of a server.</span></span>

## <span data-ttu-id="35a53-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="35a53-107">EXAMPLES</span></span>

### <span data-ttu-id="35a53-108">Przykład 1-pobiera zaawansowane zabezpieczenia danych serwera</span><span class="sxs-lookup"><span data-stu-id="35a53-108">Example 1 - Gets server Advanced Data Security</span></span>
```powershell
PS C:\>  Get-AzSqlServerAdvancedDataSecurityPolicy `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

### <span data-ttu-id="35a53-109">Przykład 2 — pobiera zaawansowane zabezpieczenia danych serwera z zasobu serwera</span><span class="sxs-lookup"><span data-stu-id="35a53-109">Example 2 - Gets server Advanced Data Security from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Get-AzSqlServerAdvancedDataSecurityPolicy

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

## <span data-ttu-id="35a53-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="35a53-110">PARAMETERS</span></span>

### <span data-ttu-id="35a53-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35a53-111">-DefaultProfile</span></span>
<span data-ttu-id="35a53-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="35a53-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35a53-113">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="35a53-113">-InputObject</span></span>
<span data-ttu-id="35a53-114">Obiekt serwera używany z operacją zaawansowanej zasady zabezpieczeń danych</span><span class="sxs-lookup"><span data-stu-id="35a53-114">The server object to use with Advanced Data Security policy operation</span></span>

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

### <span data-ttu-id="35a53-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35a53-115">-ResourceGroupName</span></span>
<span data-ttu-id="35a53-116">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="35a53-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="35a53-117">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="35a53-117">-ServerName</span></span>
<span data-ttu-id="35a53-118">Nazwa serwera bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="35a53-118">SQL Database server name.</span></span>

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

### <span data-ttu-id="35a53-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35a53-119">CommonParameters</span></span>
<span data-ttu-id="35a53-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35a53-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35a53-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="35a53-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35a53-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="35a53-122">INPUTS</span></span>

### <span data-ttu-id="35a53-123">Microsoft. Azure. Commands. SQL. Server. model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="35a53-123">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="35a53-124">System. String</span><span class="sxs-lookup"><span data-stu-id="35a53-124">System.String</span></span>

## <span data-ttu-id="35a53-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="35a53-125">OUTPUTS</span></span>

### <span data-ttu-id="35a53-126">Microsoft. Azure. Commands. SQL. AdvancedThreatProtection. model. ServerAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="35a53-126">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="35a53-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="35a53-127">NOTES</span></span>

## <span data-ttu-id="35a53-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="35a53-128">RELATED LINKS</span></span>
