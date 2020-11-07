---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azdiskencryptionset.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDiskEncryptionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDiskEncryptionSet.md
ms.openlocfilehash: a15dd51bad097aafcc517fbef67f89d65b076380
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93896805"
---
# <span data-ttu-id="de2c5-101">Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="de2c5-101">Remove-AzDiskEncryptionSet</span></span>

## <span data-ttu-id="de2c5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="de2c5-102">SYNOPSIS</span></span>
<span data-ttu-id="de2c5-103">Usuwa zestaw szyfrowania dysków.</span><span class="sxs-lookup"><span data-stu-id="de2c5-103">Removes a disk encryption set.</span></span>

## <span data-ttu-id="de2c5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="de2c5-104">SYNTAX</span></span>

### <span data-ttu-id="de2c5-105">DefaultParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="de2c5-105">DefaultParameter (Default)</span></span>
```
Remove-AzDiskEncryptionSet [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de2c5-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="de2c5-106">ResourceIdParameter</span></span>
```
Remove-AzDiskEncryptionSet [-Force] [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de2c5-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="de2c5-107">ObjectParameter</span></span>
```
Remove-AzDiskEncryptionSet [-Force] [-InputObject] <PSDiskEncryptionSet> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de2c5-108">Opis</span><span class="sxs-lookup"><span data-stu-id="de2c5-108">DESCRIPTION</span></span>
<span data-ttu-id="de2c5-109">Usuwa zestaw szyfrowania dysków.</span><span class="sxs-lookup"><span data-stu-id="de2c5-109">Removes a disk encryption set.</span></span>

## <span data-ttu-id="de2c5-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="de2c5-110">EXAMPLES</span></span>

### <span data-ttu-id="de2c5-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="de2c5-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDiskEncryptionSet -ResourceGroupName 'rg1' -Name 'enc1' -Force;
```

<span data-ttu-id="de2c5-112">Usuń szyfrowanie dysków Set "enc1" w "RG1"</span><span class="sxs-lookup"><span data-stu-id="de2c5-112">Delete disk encryption set 'enc1' in 'rg1'</span></span>

## <span data-ttu-id="de2c5-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="de2c5-113">PARAMETERS</span></span>

### <span data-ttu-id="de2c5-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="de2c5-114">-AsJob</span></span>
<span data-ttu-id="de2c5-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="de2c5-115">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de2c5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de2c5-116">-DefaultProfile</span></span>
<span data-ttu-id="de2c5-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="de2c5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de2c5-118">-Force</span><span class="sxs-lookup"><span data-stu-id="de2c5-118">-Force</span></span>
<span data-ttu-id="de2c5-119">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="de2c5-119">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de2c5-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="de2c5-120">-InputObject</span></span>
<span data-ttu-id="de2c5-121">Lokalny obiekt zestawu do szyfrowania dysków.</span><span class="sxs-lookup"><span data-stu-id="de2c5-121">The local object of the disk encryption set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet
Parameter Sets: ObjectParameter
Aliases: DiskEncryptionSet

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="de2c5-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="de2c5-122">-Name</span></span>
<span data-ttu-id="de2c5-123">Nazwa zestawu szyfrowania dysków.</span><span class="sxs-lookup"><span data-stu-id="de2c5-123">Name of disk encryption set.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: DiskEncryptionSetName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de2c5-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de2c5-124">-ResourceGroupName</span></span>
<span data-ttu-id="de2c5-125">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="de2c5-125">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de2c5-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="de2c5-126">-ResourceId</span></span>
<span data-ttu-id="de2c5-127">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="de2c5-127">The ID of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de2c5-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="de2c5-128">-Confirm</span></span>
<span data-ttu-id="de2c5-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="de2c5-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de2c5-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de2c5-130">-WhatIf</span></span>
<span data-ttu-id="de2c5-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="de2c5-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de2c5-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="de2c5-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de2c5-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de2c5-133">CommonParameters</span></span>
<span data-ttu-id="de2c5-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de2c5-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de2c5-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="de2c5-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de2c5-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="de2c5-136">INPUTS</span></span>

### <span data-ttu-id="de2c5-137">System. String</span><span class="sxs-lookup"><span data-stu-id="de2c5-137">System.String</span></span>

### <span data-ttu-id="de2c5-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="de2c5-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="de2c5-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="de2c5-139">OUTPUTS</span></span>

### <span data-ttu-id="de2c5-140">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="de2c5-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="de2c5-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="de2c5-141">NOTES</span></span>

## <span data-ttu-id="de2c5-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="de2c5-142">RELATED LINKS</span></span>
