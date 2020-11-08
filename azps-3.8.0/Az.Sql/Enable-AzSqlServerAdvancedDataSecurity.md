---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/enable-azsqlserveradvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlServerAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlServerAdvancedDataSecurity.md
ms.openlocfilehash: 36efc8b3dfec4bcc126191d68c04c2cd5d071fbd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050546"
---
# <span data-ttu-id="53a90-101">Enable-AzSqlServerAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="53a90-101">Enable-AzSqlServerAdvancedDataSecurity</span></span>

## <span data-ttu-id="53a90-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="53a90-102">SYNOPSIS</span></span>
<span data-ttu-id="53a90-103">Włączanie zaawansowanych zabezpieczeń danych na serwerze.</span><span class="sxs-lookup"><span data-stu-id="53a90-103">Enables Advanced Data Security on a server.</span></span>

## <span data-ttu-id="53a90-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="53a90-104">SYNTAX</span></span>

```
Enable-AzSqlServerAdvancedDataSecurity [-DoNotConfigureVulnerabilityAssessment] [-AsJob]
 [-DeploymentName <String>] [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="53a90-105">Opis</span><span class="sxs-lookup"><span data-stu-id="53a90-105">DESCRIPTION</span></span>
<span data-ttu-id="53a90-106">Polecenie cmdlet **enable-AzSqlServerAdvancedDataSecurity** włącza zaawansowane zabezpieczenia danych na serwerze.</span><span class="sxs-lookup"><span data-stu-id="53a90-106">The **Enable-AzSqlServerAdvancedDataSecurity** cmdlet enables Advanced Data Security on a server.</span></span> <span data-ttu-id="53a90-107">Zaawansowane zabezpieczenia danych to ujednolicony pakiet zabezpieczeń, który obejmuje klasyfikację danych, ocenę luk i zaawansowaną ochronę przed zagrożeniami dla serwera.</span><span class="sxs-lookup"><span data-stu-id="53a90-107">Advanced Data Security is a unified security package that includes Data Classification, Vulnerability Assessment and Advanced Threat Protection for your server.</span></span> <span data-ttu-id="53a90-108">(Nowe konto magazynu zostanie automatycznie utworzone w celu zapisania ocen dotyczących luk.</span><span class="sxs-lookup"><span data-stu-id="53a90-108">(A new storage account will automatically be created for saving vulnerability assessments.</span></span> <span data-ttu-id="53a90-109">Jeśli w tym celu utworzono wcześniej konto magazynu, zamiast tego zostanie użyte to polecenie.</span><span class="sxs-lookup"><span data-stu-id="53a90-109">If a storage account was previously created for this purpose, it will be used instead)</span></span>

## <span data-ttu-id="53a90-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="53a90-110">EXAMPLES</span></span>

### <span data-ttu-id="53a90-111">Przykład 1-Włączanie zaawansowanych zabezpieczeń danych serwera</span><span class="sxs-lookup"><span data-stu-id="53a90-111">Example 1 - Enable server Advanced Data Security</span></span>
```powershell
PS C:\>  Enable-AzSqlServerAdvancedDataSecurity `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

### <span data-ttu-id="53a90-112">Przykład 2 — Włączanie zaawansowanych zabezpieczeń danych serwera z zasobu serwera</span><span class="sxs-lookup"><span data-stu-id="53a90-112">Example 2 - Enable server Advanced Data Security from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Enable-AzSqlServerAdvancedDataSecurity

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

## <span data-ttu-id="53a90-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="53a90-113">PARAMETERS</span></span>

### <span data-ttu-id="53a90-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="53a90-114">-AsJob</span></span>
<span data-ttu-id="53a90-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="53a90-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="53a90-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53a90-116">-DefaultProfile</span></span>
<span data-ttu-id="53a90-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="53a90-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53a90-118">-Deploymentname</span><span class="sxs-lookup"><span data-stu-id="53a90-118">-DeploymentName</span></span>
<span data-ttu-id="53a90-119">Podaj nazwę niestandardową dla zaawansowanego wdrożenia zabezpieczeń danych</span><span class="sxs-lookup"><span data-stu-id="53a90-119">Supply a custom name for Advanced Data Security deployment</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53a90-120">-DoNotConfigureVulnerabilityAssessment</span><span class="sxs-lookup"><span data-stu-id="53a90-120">-DoNotConfigureVulnerabilityAssessment</span></span>
<span data-ttu-id="53a90-121">Nie włączaj automatycznie oceny luki (nie spowoduje to utworzenia konta magazynu)</span><span class="sxs-lookup"><span data-stu-id="53a90-121">Do not auto enable Vulnerability Assessment (This will not create a storage account)</span></span>

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

### <span data-ttu-id="53a90-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="53a90-122">-InputObject</span></span>
<span data-ttu-id="53a90-123">Obiekt serwera używany z operacją zaawansowanej zasady zabezpieczeń danych</span><span class="sxs-lookup"><span data-stu-id="53a90-123">The server object to use with Advanced Data Security policy operation</span></span>

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

### <span data-ttu-id="53a90-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53a90-124">-ResourceGroupName</span></span>
<span data-ttu-id="53a90-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="53a90-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="53a90-126">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="53a90-126">-ServerName</span></span>
<span data-ttu-id="53a90-127">Nazwa serwera bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="53a90-127">SQL Database server name.</span></span>

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

### <span data-ttu-id="53a90-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="53a90-128">-Confirm</span></span>
<span data-ttu-id="53a90-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53a90-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53a90-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53a90-130">-WhatIf</span></span>
<span data-ttu-id="53a90-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53a90-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53a90-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="53a90-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53a90-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53a90-133">CommonParameters</span></span>
<span data-ttu-id="53a90-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53a90-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53a90-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="53a90-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53a90-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="53a90-136">INPUTS</span></span>

### <span data-ttu-id="53a90-137">Microsoft. Azure. Commands. SQL. Server. model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="53a90-137">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="53a90-138">System. String</span><span class="sxs-lookup"><span data-stu-id="53a90-138">System.String</span></span>

## <span data-ttu-id="53a90-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="53a90-139">OUTPUTS</span></span>

### <span data-ttu-id="53a90-140">Microsoft. Azure. Commands. SQL. AdvancedThreatProtection. model. ServerAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="53a90-140">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="53a90-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="53a90-141">NOTES</span></span>

## <span data-ttu-id="53a90-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="53a90-142">RELATED LINKS</span></span>
