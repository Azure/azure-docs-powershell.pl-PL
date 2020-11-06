---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Grant-AzureRmSnapshotAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Grant-AzureRmSnapshotAccess.md
ms.openlocfilehash: 9b870214362c6e2bcd7225ef5a40ed5ff780139a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546271"
---
# <span data-ttu-id="f2e12-101">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="f2e12-101">Grant-AzureRmSnapshotAccess</span></span>

## <span data-ttu-id="f2e12-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f2e12-102">SYNOPSIS</span></span>
<span data-ttu-id="f2e12-103">Udziela dostępu do migawki.</span><span class="sxs-lookup"><span data-stu-id="f2e12-103">Grants an access to a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f2e12-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f2e12-104">SYNTAX</span></span>

```
Grant-AzureRmSnapshotAccess [-ResourceGroupName] <String> [-SnapshotName] <String> [[-Access] <AccessLevel>]
 [[-DurationInSecond] <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f2e12-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f2e12-105">DESCRIPTION</span></span>
<span data-ttu-id="f2e12-106">Polecenie cmdlet **Grant-AzureRmSnapshotAccess** umożliwia uzyskanie dostępu do migawki.</span><span class="sxs-lookup"><span data-stu-id="f2e12-106">The **Grant-AzureRmSnapshotAccess** cmdlet grants an access to a snapshot.</span></span>

## <span data-ttu-id="f2e12-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f2e12-107">EXAMPLES</span></span>

### <span data-ttu-id="f2e12-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f2e12-108">Example 1</span></span>
```
PS C:\> Grant-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Access 'Read' -DurationInSecond 60;
```

<span data-ttu-id="f2e12-109">Udziel uprawnienia "Odczyt" do migawki o nazwie "Snapshot01" w grupie zasobów o nazwie "ResourceGroup01" przez 60 sekund.</span><span class="sxs-lookup"><span data-stu-id="f2e12-109">Grant 'Read' access to the snapshot named 'Snapshot01' in the resource group named 'ResourceGroup01' for 60 seconds.</span></span>

## <span data-ttu-id="f2e12-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f2e12-110">PARAMETERS</span></span>

### <span data-ttu-id="f2e12-111">— Dostęp</span><span class="sxs-lookup"><span data-stu-id="f2e12-111">-Access</span></span>
<span data-ttu-id="f2e12-112">Określa poziom dostępu.</span><span class="sxs-lookup"><span data-stu-id="f2e12-112">Specifies Access level.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.AccessLevel
Parameter Sets: (All)
Aliases: 
Accepted values: None, Read

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2e12-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2e12-113">-DefaultProfile</span></span>
<span data-ttu-id="f2e12-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f2e12-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f2e12-115">-DurationInSecond</span><span class="sxs-lookup"><span data-stu-id="f2e12-115">-DurationInSecond</span></span>
<span data-ttu-id="f2e12-116">Określa czas trwania dostępu w sekundach.</span><span class="sxs-lookup"><span data-stu-id="f2e12-116">Specifies access duration in seconds.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2e12-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2e12-117">-ResourceGroupName</span></span>
<span data-ttu-id="f2e12-118">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f2e12-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="f2e12-119">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="f2e12-119">-SnapshotName</span></span>
<span data-ttu-id="f2e12-120">Określa nazwę migawki.</span><span class="sxs-lookup"><span data-stu-id="f2e12-120">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="f2e12-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f2e12-121">-Confirm</span></span>
<span data-ttu-id="f2e12-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2e12-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2e12-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2e12-123">-WhatIf</span></span>
<span data-ttu-id="f2e12-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2e12-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f2e12-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f2e12-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2e12-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2e12-126">CommonParameters</span></span>
<span data-ttu-id="f2e12-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2e12-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2e12-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2e12-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2e12-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f2e12-129">INPUTS</span></span>

### <span data-ttu-id="f2e12-130">System. String</span><span class="sxs-lookup"><span data-stu-id="f2e12-130">System.String</span></span>

## <span data-ttu-id="f2e12-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f2e12-131">OUTPUTS</span></span>

### <span data-ttu-id="f2e12-132">System. Object</span><span class="sxs-lookup"><span data-stu-id="f2e12-132">System.Object</span></span>

## <span data-ttu-id="f2e12-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f2e12-133">NOTES</span></span>

## <span data-ttu-id="f2e12-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f2e12-134">RELATED LINKS</span></span>

