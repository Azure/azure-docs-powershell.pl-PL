---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/set-azsqlvmconfiggroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Set-AzSqlVMConfigGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Set-AzSqlVMConfigGroup.md
ms.openlocfilehash: b83dc58161791009a3adfd7cbf9b0b07b3f0b5b1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176691"
---
# <span data-ttu-id="3cb86-101">Set-AzSqlVMConfigGroup</span><span class="sxs-lookup"><span data-stu-id="3cb86-101">Set-AzSqlVMConfigGroup</span></span>

## <span data-ttu-id="3cb86-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3cb86-102">SYNOPSIS</span></span>
<span data-ttu-id="3cb86-103">Ustaw informacje dotyczące grupy maszyn wirtualnych języka SQL w konfiguracji maszyny wirtualnej sql.</span><span class="sxs-lookup"><span data-stu-id="3cb86-103">Set the information relative to a sql virtual machine group in a sql virtual machine configuration.</span></span>

## <span data-ttu-id="3cb86-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="3cb86-104">SYNTAX</span></span>

```
Set-AzSqlVMConfigGroup [-SqlVM] <AzureSqlVMModel> [-SqlVMGroup] <AzureSqlVMGroupModel>
 -ClusterOperatorAccountPassword <SecureString> -SqlServiceAccountPassword <SecureString>
 [-ClusterBootstrapAccountPassword <SecureString>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3cb86-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="3cb86-105">DESCRIPTION</span></span>
<span data-ttu-id="3cb86-106">Polecenie Set-AzSqlVMConfigGroup cmdlet ustawia informacje potrzebne do dołączenia do grupy maszyn wirtualnych języka SQL w celu skonfigurowania maszyny wirtualnej sql.</span><span class="sxs-lookup"><span data-stu-id="3cb86-106">The Set-AzSqlVMConfigGroup cmdlet set the information needed in order to join a sql virtual machine group for a sql virtual machine configuration.</span></span>

## <span data-ttu-id="3cb86-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="3cb86-107">EXAMPLES</span></span>

### <span data-ttu-id="3cb86-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3cb86-108">Example 1</span></span>
```powershell
PS C:\> $config = Set-AzSqlVMConfigGroup -SqlVM $config -SqlVMGroup $group -ClusterOperatorAccountPassword 'password' -SqlServiceAccountPassword 'password'
```

<span data-ttu-id="3cb86-109">Zaktualizuj informacje o grupie konfiguracji maszyny wirtualnej sql.</span><span class="sxs-lookup"><span data-stu-id="3cb86-109">Update the group informations of a sql virtual machine configuration.</span></span>

## <span data-ttu-id="3cb86-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3cb86-110">PARAMETERS</span></span>

### <span data-ttu-id="3cb86-111">-ClusterBootstrapAccountPassword</span><span class="sxs-lookup"><span data-stu-id="3cb86-111">-ClusterBootstrapAccountPassword</span></span>
<span data-ttu-id="3cb86-112">Hasło dla konta bootstrap klastrów</span><span class="sxs-lookup"><span data-stu-id="3cb86-112">Password for the cluster bootstrap account</span></span>

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

### <span data-ttu-id="3cb86-113">-ClusterOperatorAccountPassword</span><span class="sxs-lookup"><span data-stu-id="3cb86-113">-ClusterOperatorAccountPassword</span></span>
<span data-ttu-id="3cb86-114">Hasło dla konta operatora klastrów</span><span class="sxs-lookup"><span data-stu-id="3cb86-114">Password for the cluster operator account</span></span>

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

### <span data-ttu-id="3cb86-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cb86-115">-DefaultProfile</span></span>
<span data-ttu-id="3cb86-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="3cb86-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3cb86-117">-SqlServiceAccountPassword</span><span class="sxs-lookup"><span data-stu-id="3cb86-117">-SqlServiceAccountPassword</span></span>
<span data-ttu-id="3cb86-118">Hasło do konta usługi SQL</span><span class="sxs-lookup"><span data-stu-id="3cb86-118">Password for the SQL service account</span></span>

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

### <span data-ttu-id="3cb86-119">-SqlVM</span><span class="sxs-lookup"><span data-stu-id="3cb86-119">-SqlVM</span></span>
<span data-ttu-id="3cb86-120">Konfiguracja maszyny wirtualnej SQL, do której zostanie dodane członkostwo w grupach</span><span class="sxs-lookup"><span data-stu-id="3cb86-120">The SQL virtual machine configuration which group membership will be added to</span></span>

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

### <span data-ttu-id="3cb86-121">-SqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="3cb86-121">-SqlVMGroup</span></span>
<span data-ttu-id="3cb86-122">Grupa, do których należy wirtualna maszyna SQL</span><span class="sxs-lookup"><span data-stu-id="3cb86-122">The group the SQL virtual machine will be part of</span></span>

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

### <span data-ttu-id="3cb86-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cb86-123">CommonParameters</span></span>
<span data-ttu-id="3cb86-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3cb86-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cb86-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3cb86-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cb86-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3cb86-126">INPUTS</span></span>

### <span data-ttu-id="3cb86-127">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="3cb86-127">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="3cb86-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3cb86-128">OUTPUTS</span></span>

### <span data-ttu-id="3cb86-129">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="3cb86-129">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="3cb86-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="3cb86-130">NOTES</span></span>

## <span data-ttu-id="3cb86-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3cb86-131">RELATED LINKS</span></span>
