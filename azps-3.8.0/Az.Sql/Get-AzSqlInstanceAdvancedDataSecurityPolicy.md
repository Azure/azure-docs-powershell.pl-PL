---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstanceadvanceddatasecuritypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceAdvancedDataSecurityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceAdvancedDataSecurityPolicy.md
ms.openlocfilehash: c9427df1710ad7232cf66ce576cf2c3db409f7d0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94053256"
---
# <span data-ttu-id="958e1-101">Get-AzSqlInstanceAdvancedDataSecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="958e1-101">Get-AzSqlInstanceAdvancedDataSecurityPolicy</span></span>

## <span data-ttu-id="958e1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="958e1-102">SYNOPSIS</span></span>
<span data-ttu-id="958e1-103">Pobiera zaawansowane zasady zabezpieczeń danych wystąpienia zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="958e1-103">Gets Advanced Data Security policy of a managed instance.</span></span>

## <span data-ttu-id="958e1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="958e1-104">SYNTAX</span></span>

```
Get-AzSqlInstanceAdvancedDataSecurityPolicy [-InputObject <AzureSqlManagedInstanceModel>]
 -InstanceName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="958e1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="958e1-105">DESCRIPTION</span></span>
<span data-ttu-id="958e1-106">Polecenie cmdlet **Get-AzSqlInstanceAdvancedDataSecurityPolicy** pobiera zaawansowane zasady zabezpieczeń danych wystąpienia zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="958e1-106">The **Get-AzSqlInstanceAdvancedDataSecurityPolicy** cmdlet retrieves the Advanced Data Security policy of a managed instance.</span></span>

## <span data-ttu-id="958e1-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="958e1-107">EXAMPLES</span></span>

### <span data-ttu-id="958e1-108">Przykład 1-pobiera zaawansowane zabezpieczenia danych wystąpienia zarządzanego</span><span class="sxs-lookup"><span data-stu-id="958e1-108">Example 1 - Gets managed instance Advanced Data Security</span></span>
```powershell
PS C:\>  Get-AzSqlInstanceAdvancedDataSecurityPolicy `
            -ResourceGroupName "ResourceGroup01" `
            -InstanceName "ManagedInstance01" `

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : True
```

### <span data-ttu-id="958e1-109">Przykład 2 — pobiera zaawansowane zabezpieczenia danych wystąpienia zarządzanego zasobu wystąpienia</span><span class="sxs-lookup"><span data-stu-id="958e1-109">Example 2 - Gets managed instance Advanced Data Security from managed instance resource</span></span>
```powershell
PS C:\>  Get-AzSqlInstance `
           -ResourceGroupName "ResourceGroup01" `
           -Name "ManagedInstance01" `
           | Get-AzSqlInstanceAdvancedDataSecurityPolicy

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : True
```

## <span data-ttu-id="958e1-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="958e1-110">PARAMETERS</span></span>

### <span data-ttu-id="958e1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="958e1-111">-DefaultProfile</span></span>
<span data-ttu-id="958e1-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="958e1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="958e1-113">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="958e1-113">-InputObject</span></span>
<span data-ttu-id="958e1-114">Obiekt wystąpienia zarządzanego, który ma być używany z operacją zaawansowanej zasady zabezpieczeń danych</span><span class="sxs-lookup"><span data-stu-id="958e1-114">The managed instance object to use with Advanced Data Security policy operation</span></span>

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

### <span data-ttu-id="958e1-115">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="958e1-115">-InstanceName</span></span>
<span data-ttu-id="958e1-116">Nazwa wystąpienia zarządzanego bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="958e1-116">SQL Database managed instance name.</span></span>

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

### <span data-ttu-id="958e1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="958e1-117">-ResourceGroupName</span></span>
<span data-ttu-id="958e1-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="958e1-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="958e1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="958e1-119">CommonParameters</span></span>
<span data-ttu-id="958e1-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="958e1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="958e1-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="958e1-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="958e1-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="958e1-122">INPUTS</span></span>

### <span data-ttu-id="958e1-123">Microsoft. Azure. Commands. SQL. ManagedInstance. model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="958e1-123">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="958e1-124">System. String</span><span class="sxs-lookup"><span data-stu-id="958e1-124">System.String</span></span>

## <span data-ttu-id="958e1-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="958e1-125">OUTPUTS</span></span>

### <span data-ttu-id="958e1-126">Microsoft. Azure. Commands. SQL. AdvancedThreatProtection. model. ManagedInstanceAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="958e1-126">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ManagedInstanceAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="958e1-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="958e1-127">NOTES</span></span>

## <span data-ttu-id="958e1-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="958e1-128">RELATED LINKS</span></span>
