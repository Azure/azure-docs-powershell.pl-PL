---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azdiskencryptionset.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDiskEncryptionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDiskEncryptionSet.md
ms.openlocfilehash: a15dd51bad097aafcc517fbef67f89d65b076380
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94064267"
---
# <span data-ttu-id="41b44-101">Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="41b44-101">Remove-AzDiskEncryptionSet</span></span>

## <span data-ttu-id="41b44-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="41b44-102">SYNOPSIS</span></span>
<span data-ttu-id="41b44-103">Usuwa zestaw szyfrowania dysków.</span><span class="sxs-lookup"><span data-stu-id="41b44-103">Removes a disk encryption set.</span></span>

## <span data-ttu-id="41b44-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="41b44-104">SYNTAX</span></span>

### <span data-ttu-id="41b44-105">DefaultParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="41b44-105">DefaultParameter (Default)</span></span>
```
Remove-AzDiskEncryptionSet [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41b44-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="41b44-106">ResourceIdParameter</span></span>
```
Remove-AzDiskEncryptionSet [-Force] [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41b44-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="41b44-107">ObjectParameter</span></span>
```
Remove-AzDiskEncryptionSet [-Force] [-InputObject] <PSDiskEncryptionSet> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41b44-108">Opis</span><span class="sxs-lookup"><span data-stu-id="41b44-108">DESCRIPTION</span></span>
<span data-ttu-id="41b44-109">Usuwa zestaw szyfrowania dysków.</span><span class="sxs-lookup"><span data-stu-id="41b44-109">Removes a disk encryption set.</span></span>

## <span data-ttu-id="41b44-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="41b44-110">EXAMPLES</span></span>

### <span data-ttu-id="41b44-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="41b44-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDiskEncryptionSet -ResourceGroupName 'rg1' -Name 'enc1' -Force;
```

<span data-ttu-id="41b44-112">Usuń szyfrowanie dysków Set "enc1" w "RG1"</span><span class="sxs-lookup"><span data-stu-id="41b44-112">Delete disk encryption set 'enc1' in 'rg1'</span></span>

## <span data-ttu-id="41b44-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="41b44-113">PARAMETERS</span></span>

### <span data-ttu-id="41b44-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="41b44-114">-AsJob</span></span>
<span data-ttu-id="41b44-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="41b44-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="41b44-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41b44-116">-DefaultProfile</span></span>
<span data-ttu-id="41b44-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="41b44-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41b44-118">-Force</span><span class="sxs-lookup"><span data-stu-id="41b44-118">-Force</span></span>
<span data-ttu-id="41b44-119">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="41b44-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="41b44-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="41b44-120">-InputObject</span></span>
<span data-ttu-id="41b44-121">Lokalny obiekt zestawu do szyfrowania dysków.</span><span class="sxs-lookup"><span data-stu-id="41b44-121">The local object of the disk encryption set.</span></span>

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

### <span data-ttu-id="41b44-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="41b44-122">-Name</span></span>
<span data-ttu-id="41b44-123">Nazwa zestawu szyfrowania dysków.</span><span class="sxs-lookup"><span data-stu-id="41b44-123">Name of disk encryption set.</span></span>

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

### <span data-ttu-id="41b44-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41b44-124">-ResourceGroupName</span></span>
<span data-ttu-id="41b44-125">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="41b44-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="41b44-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="41b44-126">-ResourceId</span></span>
<span data-ttu-id="41b44-127">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="41b44-127">The ID of the resource.</span></span>

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

### <span data-ttu-id="41b44-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="41b44-128">-Confirm</span></span>
<span data-ttu-id="41b44-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="41b44-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41b44-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41b44-130">-WhatIf</span></span>
<span data-ttu-id="41b44-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="41b44-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41b44-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="41b44-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41b44-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41b44-133">CommonParameters</span></span>
<span data-ttu-id="41b44-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41b44-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41b44-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="41b44-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41b44-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="41b44-136">INPUTS</span></span>

### <span data-ttu-id="41b44-137">System. String</span><span class="sxs-lookup"><span data-stu-id="41b44-137">System.String</span></span>

### <span data-ttu-id="41b44-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="41b44-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="41b44-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="41b44-139">OUTPUTS</span></span>

### <span data-ttu-id="41b44-140">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="41b44-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="41b44-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="41b44-141">NOTES</span></span>

## <span data-ttu-id="41b44-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="41b44-142">RELATED LINKS</span></span>
