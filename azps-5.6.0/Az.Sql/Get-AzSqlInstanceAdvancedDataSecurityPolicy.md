---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlinstanceadvanceddatasecuritypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceAdvancedDataSecurityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceAdvancedDataSecurityPolicy.md
ms.openlocfilehash: 2d9fa7ef7d3763d2db1d963aa1b1cac41b711bd0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014513"
---
# <span data-ttu-id="16139-101">Get-AzSqlInstanceAdvancedDataSecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="16139-101">Get-AzSqlInstanceAdvancedDataSecurityPolicy</span></span>

## <span data-ttu-id="16139-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16139-102">SYNOPSIS</span></span>
<span data-ttu-id="16139-103">Pobiera zaawansowane zasady zabezpieczeń danych zarządzanego wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="16139-103">Gets Advanced Data Security policy of a managed instance.</span></span>

## <span data-ttu-id="16139-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="16139-104">SYNTAX</span></span>

```
Get-AzSqlInstanceAdvancedDataSecurityPolicy [-InputObject <AzureSqlManagedInstanceModel>]
 -InstanceName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="16139-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="16139-105">DESCRIPTION</span></span>
<span data-ttu-id="16139-106">Polecenie **cmdlet Get-AzSqlInstanceAdvancedDataSecurityPolicy** pobiera zasady advanced data security zarządzanego wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="16139-106">The **Get-AzSqlInstanceAdvancedDataSecurityPolicy** cmdlet retrieves the Advanced Data Security policy of a managed instance.</span></span>

## <span data-ttu-id="16139-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="16139-107">EXAMPLES</span></span>

### <span data-ttu-id="16139-108">Przykład 1. Gets managed instance Advanced Data Security</span><span class="sxs-lookup"><span data-stu-id="16139-108">Example 1: Gets managed instance Advanced Data Security</span></span>
```powershell
PS C:\>  Get-AzSqlInstanceAdvancedDataSecurityPolicy `
            -ResourceGroupName "ResourceGroup01" `
            -InstanceName "ManagedInstance01" `

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : True
```

### <span data-ttu-id="16139-109">Przykład 2. Pobiera zaawansowane zabezpieczenia danych zarządzanego wystąpienia z zasobu zarządzanych wystąpień</span><span class="sxs-lookup"><span data-stu-id="16139-109">Example 2: Gets managed instance Advanced Data Security from managed instance resource</span></span>
```powershell
PS C:\>  Get-AzSqlInstance `
           -ResourceGroupName "ResourceGroup01" `
           -Name "ManagedInstance01" `
           | Get-AzSqlInstanceAdvancedDataSecurityPolicy

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : True
```

## <span data-ttu-id="16139-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="16139-110">PARAMETERS</span></span>

### <span data-ttu-id="16139-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16139-111">-DefaultProfile</span></span>
<span data-ttu-id="16139-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="16139-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16139-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="16139-113">-InputObject</span></span>
<span data-ttu-id="16139-114">Obiekt zarządzanego wystąpienia do użycia z operacją zasad zaawansowanego zabezpieczeń danych</span><span class="sxs-lookup"><span data-stu-id="16139-114">The managed instance object to use with Advanced Data Security policy operation</span></span>

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

### <span data-ttu-id="16139-115">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="16139-115">-InstanceName</span></span>
<span data-ttu-id="16139-116">Nazwa zarządzanego wystąpienia usługi SQL Database.</span><span class="sxs-lookup"><span data-stu-id="16139-116">SQL Database managed instance name.</span></span>

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

### <span data-ttu-id="16139-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16139-117">-ResourceGroupName</span></span>
<span data-ttu-id="16139-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="16139-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="16139-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16139-119">CommonParameters</span></span>
<span data-ttu-id="16139-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16139-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16139-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="16139-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16139-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="16139-122">INPUTS</span></span>

### <span data-ttu-id="16139-123">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="16139-123">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="16139-124">System.String</span><span class="sxs-lookup"><span data-stu-id="16139-124">System.String</span></span>

## <span data-ttu-id="16139-125">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="16139-125">OUTPUTS</span></span>

### <span data-ttu-id="16139-126">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ManagedInstanceAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="16139-126">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ManagedInstanceAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="16139-127">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="16139-127">NOTES</span></span>

## <span data-ttu-id="16139-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="16139-128">RELATED LINKS</span></span>
