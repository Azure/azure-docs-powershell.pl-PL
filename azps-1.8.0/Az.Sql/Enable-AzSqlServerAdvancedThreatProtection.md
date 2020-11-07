---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/enable-azsqlserveradvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlServerAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlServerAdvancedThreatProtection.md
ms.openlocfilehash: aaaf417137bb1ec16150a2bf3d0ac88b64e70fae
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708023"
---
# <span data-ttu-id="5f816-101">Enable-AzSqlServerAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="5f816-101">Enable-AzSqlServerAdvancedThreatProtection</span></span>

## <span data-ttu-id="5f816-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5f816-102">SYNOPSIS</span></span>
<span data-ttu-id="5f816-103">Włączanie zaawansowanej ochrony przed zagrożeniami na serwerze.</span><span class="sxs-lookup"><span data-stu-id="5f816-103">Enables Advanced Threat Protection on a server.</span></span>

## <span data-ttu-id="5f816-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5f816-104">SYNTAX</span></span>

```
Enable-AzSqlServerAdvancedThreatProtection [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5f816-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5f816-105">DESCRIPTION</span></span>
<span data-ttu-id="5f816-106">Polecenie cmdlet **enable-AzSqlServerAdvancedThreatProtection** włącza zaawansowaną ochronę przed zagrożeniami na serwerze.</span><span class="sxs-lookup"><span data-stu-id="5f816-106">The **Enable-AzSqlServerAdvancedThreatProtection** cmdlet enables Advanced Threat Protection on a server.</span></span>

## <span data-ttu-id="5f816-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5f816-107">EXAMPLES</span></span>

### <span data-ttu-id="5f816-108">Przykład 1-Włączanie zaawansowanej ochrony przed zagrożeniami dla serwera</span><span class="sxs-lookup"><span data-stu-id="5f816-108">Example 1 - Enable server Advanced Threat Protection</span></span>
```powershell
PS C:\>  Enable-AzSqlServerAdvancedThreatProtection `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

### <span data-ttu-id="5f816-109">Przykład 2 — Włączanie zaawansowanej ochrony przed zagrożeniami serwera z zasobu serwera</span><span class="sxs-lookup"><span data-stu-id="5f816-109">Example 2 - Enable server Advanced Threat Protection from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Enable-AzSqlServerAdvancedThreatProtection

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

## <span data-ttu-id="5f816-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5f816-110">PARAMETERS</span></span>

### <span data-ttu-id="5f816-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f816-111">-DefaultProfile</span></span>
<span data-ttu-id="5f816-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5f816-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5f816-113">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5f816-113">-InputObject</span></span>
<span data-ttu-id="5f816-114">Obiekt serwera używany z zaawansowaną zasadą ochrony przed zagrożeniami</span><span class="sxs-lookup"><span data-stu-id="5f816-114">The server object to use with Advanced Threat Protection policy operation</span></span>

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

### <span data-ttu-id="5f816-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f816-115">-ResourceGroupName</span></span>
<span data-ttu-id="5f816-116">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5f816-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="5f816-117">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="5f816-117">-ServerName</span></span>
<span data-ttu-id="5f816-118">Nazwa serwera bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="5f816-118">SQL Database server name.</span></span>

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

### <span data-ttu-id="5f816-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5f816-119">-Confirm</span></span>
<span data-ttu-id="5f816-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5f816-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f816-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f816-121">-WhatIf</span></span>
<span data-ttu-id="5f816-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5f816-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5f816-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5f816-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5f816-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f816-124">CommonParameters</span></span>
<span data-ttu-id="5f816-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f816-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f816-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5f816-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f816-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5f816-127">INPUTS</span></span>

### <span data-ttu-id="5f816-128">Microsoft. Azure. Commands. SQL. Server. model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="5f816-128">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="5f816-129">System. String</span><span class="sxs-lookup"><span data-stu-id="5f816-129">System.String</span></span>

## <span data-ttu-id="5f816-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5f816-130">OUTPUTS</span></span>

### <span data-ttu-id="5f816-131">Microsoft. Azure. Commands. SQL. AdvancedThreatProtection. model. ServerAdvancedThreatProtectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="5f816-131">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedThreatProtectionPolicyModel</span></span>

## <span data-ttu-id="5f816-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5f816-132">NOTES</span></span>

## <span data-ttu-id="5f816-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5f816-133">RELATED LINKS</span></span>
