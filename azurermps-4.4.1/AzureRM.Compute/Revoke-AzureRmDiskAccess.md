---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Revoke-AzureRmDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Revoke-AzureRmDiskAccess.md
ms.openlocfilehash: 58cbbfd2314589fd6b28f2ff375aa268c39e63d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525614"
---
# <span data-ttu-id="fdb3f-101">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="fdb3f-101">Revoke-AzureRmDiskAccess</span></span>

## <span data-ttu-id="fdb3f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fdb3f-102">SYNOPSIS</span></span>
<span data-ttu-id="fdb3f-103">Odwołuje dostęp do dysku.</span><span class="sxs-lookup"><span data-stu-id="fdb3f-103">Revokes an access to a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fdb3f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fdb3f-104">SYNTAX</span></span>

```
Revoke-AzureRmDiskAccess [-ResourceGroupName] <String> [-DiskName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fdb3f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="fdb3f-105">DESCRIPTION</span></span>
<span data-ttu-id="fdb3f-106">Polecenie cmdlet **REVOKE-AzureRmDiskAccess** odwołuje dostęp do dysku.</span><span class="sxs-lookup"><span data-stu-id="fdb3f-106">The **Revoke-AzureRmDiskAccess** cmdlet revokes an access to a disk.</span></span>

## <span data-ttu-id="fdb3f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fdb3f-107">EXAMPLES</span></span>

### <span data-ttu-id="fdb3f-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="fdb3f-108">Example 1</span></span>
```
PS C:\> Revoke-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
```

<span data-ttu-id="fdb3f-109">Odwoływanie dostępu do dysku o nazwie "Disk01" w grupie zasobów o nazwie "ResourceGroup01"</span><span class="sxs-lookup"><span data-stu-id="fdb3f-109">Revoke the access to the disk named 'Disk01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="fdb3f-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fdb3f-110">PARAMETERS</span></span>

### <span data-ttu-id="fdb3f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdb3f-111">-DefaultProfile</span></span>
<span data-ttu-id="fdb3f-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fdb3f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fdb3f-113">-Diskname</span><span class="sxs-lookup"><span data-stu-id="fdb3f-113">-DiskName</span></span>
<span data-ttu-id="fdb3f-114">Określa nazwę dysku.</span><span class="sxs-lookup"><span data-stu-id="fdb3f-114">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="fdb3f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fdb3f-115">-ResourceGroupName</span></span>
<span data-ttu-id="fdb3f-116">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="fdb3f-116">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="fdb3f-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fdb3f-117">-Confirm</span></span>
<span data-ttu-id="fdb3f-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fdb3f-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fdb3f-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fdb3f-119">-WhatIf</span></span>
<span data-ttu-id="fdb3f-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fdb3f-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fdb3f-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="fdb3f-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fdb3f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdb3f-122">CommonParameters</span></span>
<span data-ttu-id="fdb3f-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fdb3f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdb3f-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fdb3f-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdb3f-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fdb3f-125">INPUTS</span></span>

### <span data-ttu-id="fdb3f-126">System. String</span><span class="sxs-lookup"><span data-stu-id="fdb3f-126">System.String</span></span>

## <span data-ttu-id="fdb3f-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fdb3f-127">OUTPUTS</span></span>

### <span data-ttu-id="fdb3f-128">System. Object</span><span class="sxs-lookup"><span data-stu-id="fdb3f-128">System.Object</span></span>

## <span data-ttu-id="fdb3f-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fdb3f-129">NOTES</span></span>

## <span data-ttu-id="fdb3f-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fdb3f-130">RELATED LINKS</span></span>

