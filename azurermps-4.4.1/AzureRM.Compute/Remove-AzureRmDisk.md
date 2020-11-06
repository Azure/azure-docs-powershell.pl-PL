---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmDisk.md
ms.openlocfilehash: bcfba4bb002d7982f9a0fb9220fbce24e12e6ffb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553969"
---
# <span data-ttu-id="30330-101">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="30330-101">Remove-AzureRmDisk</span></span>

## <span data-ttu-id="30330-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="30330-102">SYNOPSIS</span></span>
<span data-ttu-id="30330-103">Usuwa dysk.</span><span class="sxs-lookup"><span data-stu-id="30330-103">Removes a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="30330-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="30330-104">SYNTAX</span></span>

```
Remove-AzureRmDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30330-105">Opis</span><span class="sxs-lookup"><span data-stu-id="30330-105">DESCRIPTION</span></span>
<span data-ttu-id="30330-106">Polecenie cmdlet **Remove-AzureRmDisk** usuwa dysk.</span><span class="sxs-lookup"><span data-stu-id="30330-106">The **Remove-AzureRmDisk** cmdlet removes a disk.</span></span>

## <span data-ttu-id="30330-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="30330-107">EXAMPLES</span></span>

### <span data-ttu-id="30330-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="30330-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Force;
```

<span data-ttu-id="30330-109">To polecenie usuwa dysk o nazwie "Disk01" w grupie zasobów "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="30330-109">This command removes the disk named 'Disk01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="30330-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="30330-110">PARAMETERS</span></span>

### <span data-ttu-id="30330-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30330-111">-DefaultProfile</span></span>
<span data-ttu-id="30330-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="30330-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30330-113">-Diskname</span><span class="sxs-lookup"><span data-stu-id="30330-113">-DiskName</span></span>
<span data-ttu-id="30330-114">Określa nazwę dysku.</span><span class="sxs-lookup"><span data-stu-id="30330-114">Specifies the name of a disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30330-115">-Force</span><span class="sxs-lookup"><span data-stu-id="30330-115">-Force</span></span>
<span data-ttu-id="30330-116">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="30330-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="30330-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30330-117">-ResourceGroupName</span></span>
<span data-ttu-id="30330-118">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="30330-118">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30330-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="30330-119">-Confirm</span></span>
<span data-ttu-id="30330-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="30330-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30330-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30330-121">-WhatIf</span></span>
<span data-ttu-id="30330-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="30330-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30330-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="30330-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30330-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30330-124">CommonParameters</span></span>
<span data-ttu-id="30330-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30330-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30330-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30330-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30330-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="30330-127">INPUTS</span></span>

### <span data-ttu-id="30330-128">System. String</span><span class="sxs-lookup"><span data-stu-id="30330-128">System.String</span></span>

## <span data-ttu-id="30330-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="30330-129">OUTPUTS</span></span>

### <span data-ttu-id="30330-130">System. Object</span><span class="sxs-lookup"><span data-stu-id="30330-130">System.Object</span></span>

## <span data-ttu-id="30330-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="30330-131">NOTES</span></span>

## <span data-ttu-id="30330-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="30330-132">RELATED LINKS</span></span>

