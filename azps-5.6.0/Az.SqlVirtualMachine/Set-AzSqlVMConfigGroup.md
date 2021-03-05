---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/powershell/module/az.sqlvirtualmachine/set-azsqlvmconfiggroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Set-AzSqlVMConfigGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Set-AzSqlVMConfigGroup.md
ms.openlocfilehash: 4dd2042ae3c7e84b9a7a82dde19fb5848229f51c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967265"
---
# <span data-ttu-id="c9104-101">Set-AzSqlVMConfigGroup</span><span class="sxs-lookup"><span data-stu-id="c9104-101">Set-AzSqlVMConfigGroup</span></span>

## <span data-ttu-id="c9104-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9104-102">SYNOPSIS</span></span>
<span data-ttu-id="c9104-103">Ustaw informacje dotyczące grupy maszyn wirtualnych języka SQL w konfiguracji maszyny wirtualnej sql.</span><span class="sxs-lookup"><span data-stu-id="c9104-103">Set the information relative to a sql virtual machine group in a sql virtual machine configuration.</span></span>

## <span data-ttu-id="c9104-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c9104-104">SYNTAX</span></span>

```
Set-AzSqlVMConfigGroup [-SqlVM] <AzureSqlVMModel> [-SqlVMGroup] <AzureSqlVMGroupModel>
 -ClusterOperatorAccountPassword <SecureString> -SqlServiceAccountPassword <SecureString>
 [-ClusterBootstrapAccountPassword <SecureString>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c9104-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="c9104-105">DESCRIPTION</span></span>
<span data-ttu-id="c9104-106">Polecenie Set-AzSqlVMConfigGroup cmdlet ustawia informacje potrzebne do dołączenia do grupy maszyn wirtualnych języka SQL w celu skonfigurowania maszyny wirtualnej sql.</span><span class="sxs-lookup"><span data-stu-id="c9104-106">The Set-AzSqlVMConfigGroup cmdlet set the information needed in order to join a sql virtual machine group for a sql virtual machine configuration.</span></span>

## <span data-ttu-id="c9104-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c9104-107">EXAMPLES</span></span>

### <span data-ttu-id="c9104-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c9104-108">Example 1</span></span>
```powershell
PS C:\> $config = Set-AzSqlVMConfigGroup -SqlVM $config -SqlVMGroup $group -ClusterOperatorAccountPassword 'password' -SqlServiceAccountPassword 'password'
```

<span data-ttu-id="c9104-109">Zaktualizuj informacje o grupie konfiguracji maszyny wirtualnej sql.</span><span class="sxs-lookup"><span data-stu-id="c9104-109">Update the group informations of a sql virtual machine configuration.</span></span>

## <span data-ttu-id="c9104-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c9104-110">PARAMETERS</span></span>

### <span data-ttu-id="c9104-111">-ClusterBootstrapAccountPassword</span><span class="sxs-lookup"><span data-stu-id="c9104-111">-ClusterBootstrapAccountPassword</span></span>
<span data-ttu-id="c9104-112">Hasło dla konta bootstrap klastrów</span><span class="sxs-lookup"><span data-stu-id="c9104-112">Password for the cluster bootstrap account</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9104-113">-ClusterOperatorAccountPassword</span><span class="sxs-lookup"><span data-stu-id="c9104-113">-ClusterOperatorAccountPassword</span></span>
<span data-ttu-id="c9104-114">Hasło dla konta operatora klastrów</span><span class="sxs-lookup"><span data-stu-id="c9104-114">Password for the cluster operator account</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9104-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9104-115">-DefaultProfile</span></span>
<span data-ttu-id="c9104-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c9104-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9104-117">-SqlServiceAccountPassword</span><span class="sxs-lookup"><span data-stu-id="c9104-117">-SqlServiceAccountPassword</span></span>
<span data-ttu-id="c9104-118">Hasło do konta usługi SQL</span><span class="sxs-lookup"><span data-stu-id="c9104-118">Password for the SQL service account</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9104-119">-SqlVM</span><span class="sxs-lookup"><span data-stu-id="c9104-119">-SqlVM</span></span>
<span data-ttu-id="c9104-120">Konfiguracja maszyny wirtualnej SQL, do której zostanie dodane członkostwo w grupach</span><span class="sxs-lookup"><span data-stu-id="c9104-120">The SQL virtual machine configuration which group membership will be added to</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c9104-121">-SqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="c9104-121">-SqlVMGroup</span></span>
<span data-ttu-id="c9104-122">Grupa, do których należy maszynę wirtualna SQL</span><span class="sxs-lookup"><span data-stu-id="c9104-122">The group the SQL virtual machine will be part of</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9104-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9104-123">CommonParameters</span></span>
<span data-ttu-id="c9104-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9104-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9104-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c9104-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9104-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c9104-126">INPUTS</span></span>

### <span data-ttu-id="c9104-127">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="c9104-127">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="c9104-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c9104-128">OUTPUTS</span></span>

### <span data-ttu-id="c9104-129">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="c9104-129">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="c9104-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c9104-130">NOTES</span></span>

## <span data-ttu-id="c9104-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c9104-131">RELATED LINKS</span></span>
