---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/disable-azsqlinstanceadvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlInstanceAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlInstanceAdvancedDataSecurity.md
ms.openlocfilehash: 39b23c1b39121f143791667ade542080ba70ec95
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196202"
---
# <span data-ttu-id="c0ec5-101">Disable-AzSqlInstanceAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="c0ec5-101">Disable-AzSqlInstanceAdvancedDataSecurity</span></span>

## <span data-ttu-id="c0ec5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0ec5-102">SYNOPSIS</span></span>
<span data-ttu-id="c0ec5-103">Wyłącza zaawansowane zabezpieczenia danych w wystąpieniu zarządzanym.</span><span class="sxs-lookup"><span data-stu-id="c0ec5-103">Disables Advanced Data Security on a managed instance.</span></span>

## <span data-ttu-id="c0ec5-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c0ec5-104">SYNTAX</span></span>

```
Disable-AzSqlInstanceAdvancedDataSecurity [-InputObject <AzureSqlManagedInstanceModel>] -InstanceName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c0ec5-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="c0ec5-105">DESCRIPTION</span></span>
<span data-ttu-id="c0ec5-106">Polecenie cmdlet **Disable-AzSqlInstanceAdvancedDataSecurity** wyłącza zaawansowane zabezpieczenia danych w wystąpieniu zarządzanym.</span><span class="sxs-lookup"><span data-stu-id="c0ec5-106">The **Disable-AzSqlInstanceAdvancedDataSecurity** cmdlet disables Advanced Data Security on a managed instance.</span></span>

## <span data-ttu-id="c0ec5-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c0ec5-107">EXAMPLES</span></span>

### <span data-ttu-id="c0ec5-108">Przykład 1. Wyłączanie zaawansowanego zabezpieczeń danych zarządzanego wystąpienia</span><span class="sxs-lookup"><span data-stu-id="c0ec5-108">Example 1 - Disable managed instance Advanced Data Security</span></span>
```powershell
PS C:\>  Disable-AzSqlInstanceAdvancedDataSecurity `
            -ResourceGroupName "ResourceGroup01" `
            -InstanceName "ManagedInstance01" `

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : False
```

### <span data-ttu-id="c0ec5-109">Przykład 2. Wyłączanie zaawansowanego zabezpieczeń danych serwera z zasobu zarządzanych wystąpień</span><span class="sxs-lookup"><span data-stu-id="c0ec5-109">Example 2 - Disable server Advanced Data Security from managed instance resource</span></span>
```powershell
PS C:\>  Get-AzSqlInstance `
           -ResourceGroupName "ResourceGroup01" `
           -Name "ManagedInstance01" `
           | Disable-AzSqlInstanceAdvancedDataSecurity

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : False
```

## <span data-ttu-id="c0ec5-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c0ec5-110">PARAMETERS</span></span>

### <span data-ttu-id="c0ec5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0ec5-111">-DefaultProfile</span></span>
<span data-ttu-id="c0ec5-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c0ec5-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0ec5-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c0ec5-113">-InputObject</span></span>
<span data-ttu-id="c0ec5-114">Obiekt zarządzanego wystąpienia do użycia z operacją zasad zaawansowanego zabezpieczeń danych</span><span class="sxs-lookup"><span data-stu-id="c0ec5-114">The managed instance object to use with Advanced Data Security policy operation</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0ec5-115">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="c0ec5-115">-InstanceName</span></span>
<span data-ttu-id="c0ec5-116">Nazwa zarządzanego wystąpienia usługi SQL Database.</span><span class="sxs-lookup"><span data-stu-id="c0ec5-116">SQL Database managed instance name.</span></span>

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

### <span data-ttu-id="c0ec5-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0ec5-117">-ResourceGroupName</span></span>
<span data-ttu-id="c0ec5-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c0ec5-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="c0ec5-119">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c0ec5-119">-Confirm</span></span>
<span data-ttu-id="c0ec5-120">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c0ec5-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0ec5-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0ec5-121">-WhatIf</span></span>
<span data-ttu-id="c0ec5-122">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c0ec5-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0ec5-123">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="c0ec5-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0ec5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0ec5-124">CommonParameters</span></span>
<span data-ttu-id="c0ec5-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0ec5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0ec5-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c0ec5-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0ec5-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c0ec5-127">INPUTS</span></span>

### <span data-ttu-id="c0ec5-128">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="c0ec5-128">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="c0ec5-129">System.String</span><span class="sxs-lookup"><span data-stu-id="c0ec5-129">System.String</span></span>

## <span data-ttu-id="c0ec5-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c0ec5-130">OUTPUTS</span></span>

### <span data-ttu-id="c0ec5-131">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ManagedInstanceAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="c0ec5-131">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ManagedInstanceAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="c0ec5-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c0ec5-132">NOTES</span></span>

## <span data-ttu-id="c0ec5-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c0ec5-133">RELATED LINKS</span></span>
