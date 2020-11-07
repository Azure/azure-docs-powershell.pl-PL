---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/enable-azsqlinstanceadvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlInstanceAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlInstanceAdvancedDataSecurity.md
ms.openlocfilehash: faf93387f068c6ee8e83653d31b96a1f3ecdef70
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708024"
---
# <span data-ttu-id="4b66d-101">Enable-AzSqlInstanceAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="4b66d-101">Enable-AzSqlInstanceAdvancedDataSecurity</span></span>

## <span data-ttu-id="4b66d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4b66d-102">SYNOPSIS</span></span>
<span data-ttu-id="4b66d-103">Włącza zaawansowane zabezpieczenia danych w zarządzanym wystąpieniu.</span><span class="sxs-lookup"><span data-stu-id="4b66d-103">Enables Advanced Data Security on a managed instance.</span></span>

## <span data-ttu-id="4b66d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4b66d-104">SYNTAX</span></span>

```
Enable-AzSqlInstanceAdvancedDataSecurity [-InputObject <AzureSqlManagedInstanceModel>] -InstanceName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4b66d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4b66d-105">DESCRIPTION</span></span>
<span data-ttu-id="4b66d-106">Polecenie cmdlet **enable-AzSqlInstanceAdvancedDataSecurity** włącza zaawansowane zabezpieczenia danych w zarządzanym wystąpieniu.</span><span class="sxs-lookup"><span data-stu-id="4b66d-106">The **Enable-AzSqlInstanceAdvancedDataSecurity** cmdlet enables Advanced Data Security on a managed instance.</span></span>

## <span data-ttu-id="4b66d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4b66d-107">EXAMPLES</span></span>

### <span data-ttu-id="4b66d-108">Przykład 1-Włączanie zaawansowanych zabezpieczeń danych wystąpienia zarządzanego</span><span class="sxs-lookup"><span data-stu-id="4b66d-108">Example 1 - Enable managed instance Advanced Data Security</span></span>
```powershell
PS C:\>  Enable-AzSqlInstanceAdvancedDataSecurity `
            -ResourceGroupName "ResourceGroup01" `
            -InstanceName "ManagedInstance01" 

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : True
```

### <span data-ttu-id="4b66d-109">Przykład 2 — Włączanie zaawansowanego zabezpieczenia danych wystąpienia zarządzanego z zasobu serwera</span><span class="sxs-lookup"><span data-stu-id="4b66d-109">Example 2 - Enable managed instance Advanced Data Security from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlInstance `
           -ResourceGroupName "ResourceGroup01" `
           -Name "ManagedInstance01" `
           | Enable-AzSqlInstanceAdvancedDataSecurity

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : True
```

## <span data-ttu-id="4b66d-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4b66d-110">PARAMETERS</span></span>

### <span data-ttu-id="4b66d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b66d-111">-DefaultProfile</span></span>
<span data-ttu-id="4b66d-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4b66d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b66d-113">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="4b66d-113">-InputObject</span></span>
<span data-ttu-id="4b66d-114">Obiekt wystąpienia zarządzanego, który ma być używany z operacją zaawansowanej zasady zabezpieczeń danych</span><span class="sxs-lookup"><span data-stu-id="4b66d-114">The managed instance object to use with Advanced Data Security policy operation</span></span>

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

### <span data-ttu-id="4b66d-115">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="4b66d-115">-InstanceName</span></span>
<span data-ttu-id="4b66d-116">Nazwa wystąpienia zarządzanego bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="4b66d-116">SQL Database managed instance name.</span></span>

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

### <span data-ttu-id="4b66d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b66d-117">-ResourceGroupName</span></span>
<span data-ttu-id="4b66d-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4b66d-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="4b66d-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4b66d-119">-Confirm</span></span>
<span data-ttu-id="4b66d-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4b66d-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b66d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b66d-121">-WhatIf</span></span>
<span data-ttu-id="4b66d-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4b66d-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b66d-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4b66d-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b66d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b66d-124">CommonParameters</span></span>
<span data-ttu-id="4b66d-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b66d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b66d-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4b66d-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b66d-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4b66d-127">INPUTS</span></span>

### <span data-ttu-id="4b66d-128">Microsoft. Azure. Commands. SQL. ManagedInstance. model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="4b66d-128">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="4b66d-129">System. String</span><span class="sxs-lookup"><span data-stu-id="4b66d-129">System.String</span></span>

## <span data-ttu-id="4b66d-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4b66d-130">OUTPUTS</span></span>

### <span data-ttu-id="4b66d-131">Microsoft. Azure. Commands. SQL. AdvancedThreatProtection. model. ManagedInstanceAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="4b66d-131">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ManagedInstanceAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="4b66d-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4b66d-132">NOTES</span></span>

## <span data-ttu-id="4b66d-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4b66d-133">RELATED LINKS</span></span>
