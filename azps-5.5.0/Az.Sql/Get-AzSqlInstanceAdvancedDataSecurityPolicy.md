---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstanceadvanceddatasecuritypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceAdvancedDataSecurityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceAdvancedDataSecurityPolicy.md
ms.openlocfilehash: 8adb699375a1b53f20e6027f35772642c658928b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191066"
---
# <span data-ttu-id="b4e9b-101">Get-AzSqlInstanceAdvancedDataSecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="b4e9b-101">Get-AzSqlInstanceAdvancedDataSecurityPolicy</span></span>

## <span data-ttu-id="b4e9b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4e9b-102">SYNOPSIS</span></span>
<span data-ttu-id="b4e9b-103">Pobiera zaawansowane zasady zabezpieczeń danych zarządzanego wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="b4e9b-103">Gets Advanced Data Security policy of a managed instance.</span></span>

## <span data-ttu-id="b4e9b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b4e9b-104">SYNTAX</span></span>

```
Get-AzSqlInstanceAdvancedDataSecurityPolicy [-InputObject <AzureSqlManagedInstanceModel>]
 -InstanceName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b4e9b-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="b4e9b-105">DESCRIPTION</span></span>
<span data-ttu-id="b4e9b-106">Polecenie **cmdlet Get-AzSqlInstanceAdvancedDataSecurityPolicy** pobiera zasady advanced data security zarządzanego wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="b4e9b-106">The **Get-AzSqlInstanceAdvancedDataSecurityPolicy** cmdlet retrieves the Advanced Data Security policy of a managed instance.</span></span>

## <span data-ttu-id="b4e9b-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b4e9b-107">EXAMPLES</span></span>

### <span data-ttu-id="b4e9b-108">Przykład 1. Pobiera zarządzane wystąpienie Zaawansowane zabezpieczenia danych</span><span class="sxs-lookup"><span data-stu-id="b4e9b-108">Example 1: Gets managed instance Advanced Data Security</span></span>
```powershell
PS C:\>  Get-AzSqlInstanceAdvancedDataSecurityPolicy `
            -ResourceGroupName "ResourceGroup01" `
            -InstanceName "ManagedInstance01" `

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : True
```

### <span data-ttu-id="b4e9b-109">Przykład 2. Pobiera zaawansowane zabezpieczenia danych zarządzanego wystąpienia z zasobu zarządzanych wystąpień</span><span class="sxs-lookup"><span data-stu-id="b4e9b-109">Example 2: Gets managed instance Advanced Data Security from managed instance resource</span></span>
```powershell
PS C:\>  Get-AzSqlInstance `
           -ResourceGroupName "ResourceGroup01" `
           -Name "ManagedInstance01" `
           | Get-AzSqlInstanceAdvancedDataSecurityPolicy

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : True
```

## <span data-ttu-id="b4e9b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b4e9b-110">PARAMETERS</span></span>

### <span data-ttu-id="b4e9b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4e9b-111">-DefaultProfile</span></span>
<span data-ttu-id="b4e9b-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b4e9b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4e9b-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b4e9b-113">-InputObject</span></span>
<span data-ttu-id="b4e9b-114">Obiekt zarządzanego wystąpienia do użycia z operacją zasad zaawansowanego zabezpieczeń danych</span><span class="sxs-lookup"><span data-stu-id="b4e9b-114">The managed instance object to use with Advanced Data Security policy operation</span></span>

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

### <span data-ttu-id="b4e9b-115">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="b4e9b-115">-InstanceName</span></span>
<span data-ttu-id="b4e9b-116">Nazwa zarządzanego wystąpienia usługi SQL Database.</span><span class="sxs-lookup"><span data-stu-id="b4e9b-116">SQL Database managed instance name.</span></span>

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

### <span data-ttu-id="b4e9b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4e9b-117">-ResourceGroupName</span></span>
<span data-ttu-id="b4e9b-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b4e9b-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="b4e9b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4e9b-119">CommonParameters</span></span>
<span data-ttu-id="b4e9b-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4e9b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4e9b-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b4e9b-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4e9b-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b4e9b-122">INPUTS</span></span>

### <span data-ttu-id="b4e9b-123">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="b4e9b-123">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="b4e9b-124">System.String</span><span class="sxs-lookup"><span data-stu-id="b4e9b-124">System.String</span></span>

## <span data-ttu-id="b4e9b-125">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b4e9b-125">OUTPUTS</span></span>

### <span data-ttu-id="b4e9b-126">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ManagedInstanceAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="b4e9b-126">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ManagedInstanceAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="b4e9b-127">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b4e9b-127">NOTES</span></span>

## <span data-ttu-id="b4e9b-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b4e9b-128">RELATED LINKS</span></span>
