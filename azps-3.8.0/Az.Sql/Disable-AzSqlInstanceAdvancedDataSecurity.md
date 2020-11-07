---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/disable-azsqlinstanceadvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlInstanceAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlInstanceAdvancedDataSecurity.md
ms.openlocfilehash: 39b23c1b39121f143791667ade542080ba70ec95
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93895794"
---
# <span data-ttu-id="22844-101">Disable-AzSqlInstanceAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="22844-101">Disable-AzSqlInstanceAdvancedDataSecurity</span></span>

## <span data-ttu-id="22844-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="22844-102">SYNOPSIS</span></span>
<span data-ttu-id="22844-103">Wyłącza zaawansowane zabezpieczenia danych w zarządzanym wystąpieniu.</span><span class="sxs-lookup"><span data-stu-id="22844-103">Disables Advanced Data Security on a managed instance.</span></span>

## <span data-ttu-id="22844-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="22844-104">SYNTAX</span></span>

```
Disable-AzSqlInstanceAdvancedDataSecurity [-InputObject <AzureSqlManagedInstanceModel>] -InstanceName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="22844-105">Opis</span><span class="sxs-lookup"><span data-stu-id="22844-105">DESCRIPTION</span></span>
<span data-ttu-id="22844-106">Polecenie cmdlet **disable-AzSqlInstanceAdvancedDataSecurity** wyłącza zaawansowane zabezpieczenia danych w zarządzanym wystąpieniu.</span><span class="sxs-lookup"><span data-stu-id="22844-106">The **Disable-AzSqlInstanceAdvancedDataSecurity** cmdlet disables Advanced Data Security on a managed instance.</span></span>

## <span data-ttu-id="22844-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="22844-107">EXAMPLES</span></span>

### <span data-ttu-id="22844-108">Przykład 1-Wyłącz Zaawansowane bezpieczeństwo danych wystąpienia zarządzanego</span><span class="sxs-lookup"><span data-stu-id="22844-108">Example 1 - Disable managed instance Advanced Data Security</span></span>
```powershell
PS C:\>  Disable-AzSqlInstanceAdvancedDataSecurity `
            -ResourceGroupName "ResourceGroup01" `
            -InstanceName "ManagedInstance01" `

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : False
```

### <span data-ttu-id="22844-109">Przykład 2 — Wyłączenie zaawansowanego zabezpieczenia danych serwera z zasobu zarządzanego wystąpienia</span><span class="sxs-lookup"><span data-stu-id="22844-109">Example 2 - Disable server Advanced Data Security from managed instance resource</span></span>
```powershell
PS C:\>  Get-AzSqlInstance `
           -ResourceGroupName "ResourceGroup01" `
           -Name "ManagedInstance01" `
           | Disable-AzSqlInstanceAdvancedDataSecurity

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : False
```

## <span data-ttu-id="22844-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="22844-110">PARAMETERS</span></span>

### <span data-ttu-id="22844-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22844-111">-DefaultProfile</span></span>
<span data-ttu-id="22844-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="22844-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22844-113">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="22844-113">-InputObject</span></span>
<span data-ttu-id="22844-114">Obiekt wystąpienia zarządzanego, który ma być używany z operacją zaawansowanej zasady zabezpieczeń danych</span><span class="sxs-lookup"><span data-stu-id="22844-114">The managed instance object to use with Advanced Data Security policy operation</span></span>

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

### <span data-ttu-id="22844-115">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="22844-115">-InstanceName</span></span>
<span data-ttu-id="22844-116">Nazwa wystąpienia zarządzanego bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="22844-116">SQL Database managed instance name.</span></span>

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

### <span data-ttu-id="22844-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22844-117">-ResourceGroupName</span></span>
<span data-ttu-id="22844-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="22844-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="22844-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="22844-119">-Confirm</span></span>
<span data-ttu-id="22844-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="22844-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22844-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22844-121">-WhatIf</span></span>
<span data-ttu-id="22844-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="22844-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22844-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="22844-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22844-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22844-124">CommonParameters</span></span>
<span data-ttu-id="22844-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22844-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22844-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="22844-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22844-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="22844-127">INPUTS</span></span>

### <span data-ttu-id="22844-128">Microsoft. Azure. Commands. SQL. ManagedInstance. model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="22844-128">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="22844-129">System. String</span><span class="sxs-lookup"><span data-stu-id="22844-129">System.String</span></span>

## <span data-ttu-id="22844-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="22844-130">OUTPUTS</span></span>

### <span data-ttu-id="22844-131">Microsoft. Azure. Commands. SQL. AdvancedThreatProtection. model. ManagedInstanceAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="22844-131">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ManagedInstanceAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="22844-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="22844-132">NOTES</span></span>

## <span data-ttu-id="22844-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="22844-133">RELATED LINKS</span></span>
