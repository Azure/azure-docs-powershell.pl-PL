---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/grant-azdiskaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Grant-AzDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Grant-AzDiskAccess.md
ms.openlocfilehash: b7c5f713c7c245676804318b880df3f79a7ca60d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893682"
---
# <span data-ttu-id="4d534-101">Grant-AzDiskAccess</span><span class="sxs-lookup"><span data-stu-id="4d534-101">Grant-AzDiskAccess</span></span>

## <span data-ttu-id="4d534-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4d534-102">SYNOPSIS</span></span>
<span data-ttu-id="4d534-103">Udziela dostępu do dysku.</span><span class="sxs-lookup"><span data-stu-id="4d534-103">Grants an access to a disk.</span></span>

## <span data-ttu-id="4d534-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4d534-104">SYNTAX</span></span>

```
Grant-AzDiskAccess [-ResourceGroupName] <String> [-DiskName] <String> [-Access] <AccessLevel>
 [[-DurationInSecond] <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4d534-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4d534-105">DESCRIPTION</span></span>
<span data-ttu-id="4d534-106">Polecenie cmdlet **Grant-AzDiskAccess** umożliwia uzyskanie dostępu do dysku.</span><span class="sxs-lookup"><span data-stu-id="4d534-106">The **Grant-AzDiskAccess** cmdlet grants an access to a disk.</span></span>

## <span data-ttu-id="4d534-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4d534-107">EXAMPLES</span></span>

### <span data-ttu-id="4d534-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4d534-108">Example 1</span></span>
```
PS C:\> Grant-AzDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Access 'Read' -DurationInSecond 60;
```

<span data-ttu-id="4d534-109">Udziel uprawnienia "Odczyt" na dysk o nazwie "Disk01" w grupie zasobów o nazwie "ResourceGroup01" dla 60 sekund.</span><span class="sxs-lookup"><span data-stu-id="4d534-109">Grant 'Read' access to the disk named 'Disk01' in the resource group named 'ResourceGroup01' for 60 seconds.</span></span>

## <span data-ttu-id="4d534-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4d534-110">PARAMETERS</span></span>

### <span data-ttu-id="4d534-111">— Dostęp</span><span class="sxs-lookup"><span data-stu-id="4d534-111">-Access</span></span>
<span data-ttu-id="4d534-112">Określa poziom dostępu.</span><span class="sxs-lookup"><span data-stu-id="4d534-112">Specifies Access level.</span></span>

```yaml
Type: AccessLevel
Parameter Sets: (All)
Aliases: 
Accepted values: None, Read

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d534-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4d534-113">-AsJob</span></span>
<span data-ttu-id="4d534-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="4d534-114">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d534-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d534-115">-DefaultProfile</span></span>
<span data-ttu-id="4d534-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4d534-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d534-117">-Diskname</span><span class="sxs-lookup"><span data-stu-id="4d534-117">-DiskName</span></span>
<span data-ttu-id="4d534-118">Określa nazwę dysku.</span><span class="sxs-lookup"><span data-stu-id="4d534-118">Specifies the name of a disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d534-119">-DurationInSecond</span><span class="sxs-lookup"><span data-stu-id="4d534-119">-DurationInSecond</span></span>
<span data-ttu-id="4d534-120">Określa czas trwania dostępu w sekundach.</span><span class="sxs-lookup"><span data-stu-id="4d534-120">Specifies access duration in seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d534-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d534-121">-ResourceGroupName</span></span>
<span data-ttu-id="4d534-122">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4d534-122">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d534-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4d534-123">-Confirm</span></span>
<span data-ttu-id="4d534-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d534-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d534-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d534-125">-WhatIf</span></span>
<span data-ttu-id="4d534-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d534-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4d534-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4d534-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d534-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d534-128">CommonParameters</span></span>
<span data-ttu-id="4d534-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d534-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d534-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d534-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d534-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4d534-131">INPUTS</span></span>

### <span data-ttu-id="4d534-132">System. String</span><span class="sxs-lookup"><span data-stu-id="4d534-132">System.String</span></span>

## <span data-ttu-id="4d534-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4d534-133">OUTPUTS</span></span>

### <span data-ttu-id="4d534-134">System. Object</span><span class="sxs-lookup"><span data-stu-id="4d534-134">System.Object</span></span>

## <span data-ttu-id="4d534-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4d534-135">NOTES</span></span>

## <span data-ttu-id="4d534-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4d534-136">RELATED LINKS</span></span>

