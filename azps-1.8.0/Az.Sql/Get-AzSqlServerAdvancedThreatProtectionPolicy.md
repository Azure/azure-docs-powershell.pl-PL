---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserveradvancedthreatprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedThreatProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedThreatProtectionPolicy.md
ms.openlocfilehash: dce8018e97e01c10356e77d321d564690cc03f71
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707922"
---
# <span data-ttu-id="77153-101">Get-AzSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="77153-101">Get-AzSqlServerAdvancedThreatProtectionPolicy</span></span>

## <span data-ttu-id="77153-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="77153-102">SYNOPSIS</span></span>
<span data-ttu-id="77153-103">Pobiera zaawansowane zasady ochrony przed zagrożeniami serwera.</span><span class="sxs-lookup"><span data-stu-id="77153-103">Gets Advanced Threat Protection policy of a server.</span></span>

## <span data-ttu-id="77153-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="77153-104">SYNTAX</span></span>

```
Get-AzSqlServerAdvancedThreatProtectionPolicy [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="77153-105">Opis</span><span class="sxs-lookup"><span data-stu-id="77153-105">DESCRIPTION</span></span>
<span data-ttu-id="77153-106">Polecenie cmdlet **Get-AzSqlServerAdvancedThreatProtectionPolicy** retrives zaawansowane zasady ochrony przed zagrożeniami serwera.</span><span class="sxs-lookup"><span data-stu-id="77153-106">The **Get-AzSqlServerAdvancedThreatProtectionPolicy** cmdlet retrives the Advanced Threat Protection policy of a server.</span></span>

## <span data-ttu-id="77153-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="77153-107">EXAMPLES</span></span>

### <span data-ttu-id="77153-108">Przykład 1-pobiera zaawansowaną ochronę przed zagrożeniami serwera</span><span class="sxs-lookup"><span data-stu-id="77153-108">Example 1 - Gets server Advanced Threat Protection</span></span>
```powershell
PS C:\>  Get-AzSqlServerAdvancedThreatProtectionPolicy `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

### <span data-ttu-id="77153-109">Przykład 2 — pobiera zaawansowaną ochronę przed zagrożeniami serwera z zasobu serwera</span><span class="sxs-lookup"><span data-stu-id="77153-109">Example 2 - Gets server Advanced Threat Protection from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Get-AzSqlServerAdvancedThreatProtectionPolicy

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

## <span data-ttu-id="77153-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="77153-110">PARAMETERS</span></span>

### <span data-ttu-id="77153-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77153-111">-DefaultProfile</span></span>
<span data-ttu-id="77153-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="77153-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77153-113">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="77153-113">-InputObject</span></span>
<span data-ttu-id="77153-114">Obiekt serwera używany z zaawansowaną zasadą ochrony przed zagrożeniami</span><span class="sxs-lookup"><span data-stu-id="77153-114">The server object to use with Advanced Threat Protection policy operation</span></span>

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

### <span data-ttu-id="77153-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77153-115">-ResourceGroupName</span></span>
<span data-ttu-id="77153-116">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="77153-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="77153-117">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="77153-117">-ServerName</span></span>
<span data-ttu-id="77153-118">Nazwa serwera bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="77153-118">SQL Database server name.</span></span>

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

### <span data-ttu-id="77153-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77153-119">CommonParameters</span></span>
<span data-ttu-id="77153-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77153-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77153-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="77153-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77153-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="77153-122">INPUTS</span></span>

### <span data-ttu-id="77153-123">Microsoft. Azure. Commands. SQL. Server. model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="77153-123">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="77153-124">System. String</span><span class="sxs-lookup"><span data-stu-id="77153-124">System.String</span></span>

## <span data-ttu-id="77153-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="77153-125">OUTPUTS</span></span>

### <span data-ttu-id="77153-126">Microsoft. Azure. Commands. SQL. AdvancedThreatProtection. model. ServerAdvancedThreatProtectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="77153-126">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedThreatProtectionPolicyModel</span></span>

## <span data-ttu-id="77153-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="77153-127">NOTES</span></span>

## <span data-ttu-id="77153-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="77153-128">RELATED LINKS</span></span>
