---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/set-azsqlvmconfiggroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Set-AzSqlVMConfigGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Set-AzSqlVMConfigGroup.md
ms.openlocfilehash: b83dc58161791009a3adfd7cbf9b0b07b3f0b5b1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98334381"
---
# <span data-ttu-id="94e5d-101">Set-AzSqlVMConfigGroup</span><span class="sxs-lookup"><span data-stu-id="94e5d-101">Set-AzSqlVMConfigGroup</span></span>

## <span data-ttu-id="94e5d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="94e5d-102">SYNOPSIS</span></span>
<span data-ttu-id="94e5d-103">Ustaw informacje odnoszące się do grupy maszyn wirtualnych SQL w konfiguracji maszyny wirtualnej SQL.</span><span class="sxs-lookup"><span data-stu-id="94e5d-103">Set the information relative to a sql virtual machine group in a sql virtual machine configuration.</span></span>

## <span data-ttu-id="94e5d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="94e5d-104">SYNTAX</span></span>

```
Set-AzSqlVMConfigGroup [-SqlVM] <AzureSqlVMModel> [-SqlVMGroup] <AzureSqlVMGroupModel>
 -ClusterOperatorAccountPassword <SecureString> -SqlServiceAccountPassword <SecureString>
 [-ClusterBootstrapAccountPassword <SecureString>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="94e5d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="94e5d-105">DESCRIPTION</span></span>
<span data-ttu-id="94e5d-106">Polecenie cmdlet Set-AzSqlVMConfigGroup Ustaw informacje potrzebne do dołączenia do grupy maszyn wirtualnych SQL w konfiguracji maszyny wirtualnej SQL.</span><span class="sxs-lookup"><span data-stu-id="94e5d-106">The Set-AzSqlVMConfigGroup cmdlet set the information needed in order to join a sql virtual machine group for a sql virtual machine configuration.</span></span>

## <span data-ttu-id="94e5d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="94e5d-107">EXAMPLES</span></span>

### <span data-ttu-id="94e5d-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="94e5d-108">Example 1</span></span>
```powershell
PS C:\> $config = Set-AzSqlVMConfigGroup -SqlVM $config -SqlVMGroup $group -ClusterOperatorAccountPassword 'password' -SqlServiceAccountPassword 'password'
```

<span data-ttu-id="94e5d-109">Zaktualizuj informacje o grupie konfiguracji maszyny wirtualnej SQL.</span><span class="sxs-lookup"><span data-stu-id="94e5d-109">Update the group informations of a sql virtual machine configuration.</span></span>

## <span data-ttu-id="94e5d-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="94e5d-110">PARAMETERS</span></span>

### <span data-ttu-id="94e5d-111">-ClusterBootstrapAccountPassword</span><span class="sxs-lookup"><span data-stu-id="94e5d-111">-ClusterBootstrapAccountPassword</span></span>
<span data-ttu-id="94e5d-112">Hasło do konta uruchamiania klastra</span><span class="sxs-lookup"><span data-stu-id="94e5d-112">Password for the cluster bootstrap account</span></span>

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

### <span data-ttu-id="94e5d-113">-ClusterOperatorAccountPassword</span><span class="sxs-lookup"><span data-stu-id="94e5d-113">-ClusterOperatorAccountPassword</span></span>
<span data-ttu-id="94e5d-114">Hasło do konta operatora klastra</span><span class="sxs-lookup"><span data-stu-id="94e5d-114">Password for the cluster operator account</span></span>

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

### <span data-ttu-id="94e5d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94e5d-115">-DefaultProfile</span></span>
<span data-ttu-id="94e5d-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="94e5d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94e5d-117">-SqlServiceAccountPassword</span><span class="sxs-lookup"><span data-stu-id="94e5d-117">-SqlServiceAccountPassword</span></span>
<span data-ttu-id="94e5d-118">Hasło do konta usługi SQL</span><span class="sxs-lookup"><span data-stu-id="94e5d-118">Password for the SQL service account</span></span>

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

### <span data-ttu-id="94e5d-119">-SqlVM</span><span class="sxs-lookup"><span data-stu-id="94e5d-119">-SqlVM</span></span>
<span data-ttu-id="94e5d-120">Konfiguracja maszyny wirtualnej SQL, do której zostanie dodana przynależność do grupy</span><span class="sxs-lookup"><span data-stu-id="94e5d-120">The SQL virtual machine configuration which group membership will be added to</span></span>

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

### <span data-ttu-id="94e5d-121">-SqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="94e5d-121">-SqlVMGroup</span></span>
<span data-ttu-id="94e5d-122">Grupa, do której należy maszyna wirtualna SQL</span><span class="sxs-lookup"><span data-stu-id="94e5d-122">The group the SQL virtual machine will be part of</span></span>

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

### <span data-ttu-id="94e5d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94e5d-123">CommonParameters</span></span>
<span data-ttu-id="94e5d-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94e5d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94e5d-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="94e5d-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94e5d-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="94e5d-126">INPUTS</span></span>

### <span data-ttu-id="94e5d-127">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. model. AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="94e5d-127">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="94e5d-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="94e5d-128">OUTPUTS</span></span>

### <span data-ttu-id="94e5d-129">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. model. AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="94e5d-129">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="94e5d-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="94e5d-130">NOTES</span></span>

## <span data-ttu-id="94e5d-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="94e5d-131">RELATED LINKS</span></span>
