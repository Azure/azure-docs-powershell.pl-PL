---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/disable-azurermsqlserveradvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Disable-AzureRmSqlServerAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Disable-AzureRmSqlServerAdvancedThreatProtection.md
ms.openlocfilehash: cc38d619b810f2567594c0c1020190c271dc9f33
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543391"
---
# <span data-ttu-id="96d35-101">Disable-AzureRmSqlServerAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="96d35-101">Disable-AzureRmSqlServerAdvancedThreatProtection</span></span>

## <span data-ttu-id="96d35-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="96d35-102">SYNOPSIS</span></span>
<span data-ttu-id="96d35-103">Wyłącza zaawansowaną ochronę przed zagrożeniami na serwerze.</span><span class="sxs-lookup"><span data-stu-id="96d35-103">Disables Advanced Threat Protection on a server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="96d35-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="96d35-104">SYNTAX</span></span>

```
Disable-AzureRmSqlServerAdvancedThreatProtection [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="96d35-105">Opis</span><span class="sxs-lookup"><span data-stu-id="96d35-105">DESCRIPTION</span></span>
<span data-ttu-id="96d35-106">Polecenie cmdlet **disable-AzureRmSqlServerAdvancedThreatProtection** wyłącza zaawansowaną ochronę przed zagrożeniami na serwerze.</span><span class="sxs-lookup"><span data-stu-id="96d35-106">The **Disable-AzureRmSqlServerAdvancedThreatProtection** cmdlet disables Advanced Threat Protection on a server.</span></span>

## <span data-ttu-id="96d35-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="96d35-107">EXAMPLES</span></span>

### <span data-ttu-id="96d35-108">Przykład 1-wyłączanie zaawansowanej ochrony przed zagrożeniami dla serwera</span><span class="sxs-lookup"><span data-stu-id="96d35-108">Example 1 - Disable server Advanced Threat Protection</span></span>
```powershell
PS C:\>  Disable-AzureRmSqlServerAdvancedThreatProtection `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : False
```

### <span data-ttu-id="96d35-109">Przykład 2-Wyłączenie zaawansowanej ochrony przed zagrożeniami serwera z zasobu serwera</span><span class="sxs-lookup"><span data-stu-id="96d35-109">Example 2 - Disable server Advanced Threat Protection from server resource</span></span>
```powershell
PS C:\>  Get-AzureRmSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Disable-AzureRmSqlServerAdvancedThreatProtection

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : False
```

## <span data-ttu-id="96d35-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="96d35-110">PARAMETERS</span></span>

### <span data-ttu-id="96d35-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96d35-111">-DefaultProfile</span></span>
<span data-ttu-id="96d35-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="96d35-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96d35-113">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="96d35-113">-InputObject</span></span>
<span data-ttu-id="96d35-114">Obiekt serwera używany z zaawansowaną zasadą ochrony przed zagrożeniami</span><span class="sxs-lookup"><span data-stu-id="96d35-114">The server object to use with Advanced Threat Protection policy operation</span></span>

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

### <span data-ttu-id="96d35-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96d35-115">-ResourceGroupName</span></span>
<span data-ttu-id="96d35-116">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="96d35-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="96d35-117">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="96d35-117">-ServerName</span></span>
<span data-ttu-id="96d35-118">Nazwa serwera bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="96d35-118">SQL Database server name.</span></span>

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

### <span data-ttu-id="96d35-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="96d35-119">-Confirm</span></span>
<span data-ttu-id="96d35-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="96d35-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96d35-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96d35-121">-WhatIf</span></span>
<span data-ttu-id="96d35-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="96d35-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="96d35-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="96d35-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96d35-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96d35-124">CommonParameters</span></span>
<span data-ttu-id="96d35-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96d35-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96d35-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96d35-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96d35-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="96d35-127">INPUTS</span></span>

### <span data-ttu-id="96d35-128">Microsoft. Azure. Commands. SQL. Server. model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="96d35-128">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>
<span data-ttu-id="96d35-129">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="96d35-129">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="96d35-130">System. String</span><span class="sxs-lookup"><span data-stu-id="96d35-130">System.String</span></span>

## <span data-ttu-id="96d35-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="96d35-131">OUTPUTS</span></span>

### <span data-ttu-id="96d35-132">Microsoft. Azure. Commands. SQL. AdvancedThreatProtection. model. ServerAdvancedThreatProtectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="96d35-132">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedThreatProtectionPolicyModel</span></span>

## <span data-ttu-id="96d35-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="96d35-133">NOTES</span></span>

## <span data-ttu-id="96d35-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="96d35-134">RELATED LINKS</span></span>
