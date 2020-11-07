---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/disable-azsqlinstanceadvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlInstanceAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlInstanceAdvancedDataSecurity.md
ms.openlocfilehash: 872189e5219b1e4d7079664d190450ed2dd4bebb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708026"
---
# <span data-ttu-id="e49e6-101">Disable-AzSqlInstanceAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="e49e6-101">Disable-AzSqlInstanceAdvancedDataSecurity</span></span>

## <span data-ttu-id="e49e6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e49e6-102">SYNOPSIS</span></span>
<span data-ttu-id="e49e6-103">Wyłącza zaawansowane zabezpieczenia danych w zarządzanym wystąpieniu.</span><span class="sxs-lookup"><span data-stu-id="e49e6-103">Disables Advanced Data Security on a managed instance.</span></span>

## <span data-ttu-id="e49e6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e49e6-104">SYNTAX</span></span>

```
Disable-AzSqlInstanceAdvancedDataSecurity [-InputObject <AzureSqlManagedInstanceModel>] -InstanceName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e49e6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e49e6-105">DESCRIPTION</span></span>
<span data-ttu-id="e49e6-106">Polecenie cmdlet **disable-AzSqlInstanceAdvancedDataSecurity** wyłącza zaawansowane zabezpieczenia danych w zarządzanym wystąpieniu.</span><span class="sxs-lookup"><span data-stu-id="e49e6-106">The **Disable-AzSqlInstanceAdvancedDataSecurity** cmdlet disables Advanced Data Security on a managed instance.</span></span>

## <span data-ttu-id="e49e6-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e49e6-107">EXAMPLES</span></span>

### <span data-ttu-id="e49e6-108">Przykład 1-Wyłącz Zaawansowane bezpieczeństwo danych wystąpienia zarządzanego</span><span class="sxs-lookup"><span data-stu-id="e49e6-108">Example 1 - Disable managed instance Advanced Data Security</span></span>
```powershell
PS C:\>  Disable-AzSqlInstanceAdvancedDataSecurity `
            -ResourceGroupName "ResourceGroup01" `
            -InstanceName "ManagedInstance01" `

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : False
```

### <span data-ttu-id="e49e6-109">Przykład 2 — Wyłączenie zaawansowanego zabezpieczenia danych serwera z zasobu zarządzanego wystąpienia</span><span class="sxs-lookup"><span data-stu-id="e49e6-109">Example 2 - Disable server Advanced Data Security from managed instance resource</span></span>
```powershell
PS C:\>  Get-AzSqlInstance `
           -ResourceGroupName "ResourceGroup01" `
           -Name "ManagedInstance01" `
           | Disable-AzSqlInstanceAdvancedDataSecurity

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : False
```

## <span data-ttu-id="e49e6-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e49e6-110">PARAMETERS</span></span>

### <span data-ttu-id="e49e6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e49e6-111">-DefaultProfile</span></span>
<span data-ttu-id="e49e6-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e49e6-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e49e6-113">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e49e6-113">-InputObject</span></span>
<span data-ttu-id="e49e6-114">Obiekt wystąpienia zarządzanego, który ma być używany z operacją zaawansowanej zasady zabezpieczeń danych</span><span class="sxs-lookup"><span data-stu-id="e49e6-114">The managed instance object to use with Advanced Data Security policy operation</span></span>

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

### <span data-ttu-id="e49e6-115">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="e49e6-115">-InstanceName</span></span>
<span data-ttu-id="e49e6-116">Nazwa wystąpienia zarządzanego bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="e49e6-116">SQL Database managed instance name.</span></span>

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

### <span data-ttu-id="e49e6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e49e6-117">-ResourceGroupName</span></span>
<span data-ttu-id="e49e6-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e49e6-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="e49e6-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e49e6-119">-Confirm</span></span>
<span data-ttu-id="e49e6-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e49e6-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e49e6-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e49e6-121">-WhatIf</span></span>
<span data-ttu-id="e49e6-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e49e6-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e49e6-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e49e6-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e49e6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e49e6-124">CommonParameters</span></span>
<span data-ttu-id="e49e6-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e49e6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e49e6-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e49e6-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e49e6-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e49e6-127">INPUTS</span></span>

### <span data-ttu-id="e49e6-128">Microsoft. Azure. Commands. SQL. ManagedInstance. model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="e49e6-128">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="e49e6-129">System. String</span><span class="sxs-lookup"><span data-stu-id="e49e6-129">System.String</span></span>

## <span data-ttu-id="e49e6-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e49e6-130">OUTPUTS</span></span>

### <span data-ttu-id="e49e6-131">Microsoft. Azure. Commands. SQL. AdvancedThreatProtection. model. ManagedInstanceAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="e49e6-131">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ManagedInstanceAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="e49e6-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e49e6-132">NOTES</span></span>

## <span data-ttu-id="e49e6-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e49e6-133">RELATED LINKS</span></span>
