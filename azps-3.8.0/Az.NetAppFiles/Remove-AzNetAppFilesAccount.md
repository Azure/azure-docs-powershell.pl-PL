---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesAccount.md
ms.openlocfilehash: de0f71a91ec4445ae4be58e904e58eb3a97cb9a0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93894190"
---
# <span data-ttu-id="8fd85-101">Remove-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="8fd85-101">Remove-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="8fd85-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8fd85-102">SYNOPSIS</span></span>
<span data-ttu-id="8fd85-103">Usuwa konto usługi Azure NetApp Files (ANF).</span><span class="sxs-lookup"><span data-stu-id="8fd85-103">Deletes an Azure NetApp Files (ANF) account.</span></span>

## <span data-ttu-id="8fd85-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8fd85-104">SYNTAX</span></span>

### <span data-ttu-id="8fd85-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8fd85-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesAccount -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8fd85-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8fd85-106">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesAccount -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8fd85-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8fd85-107">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesAccount -InputObject <PSNetAppFilesAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8fd85-108">Opis</span><span class="sxs-lookup"><span data-stu-id="8fd85-108">DESCRIPTION</span></span>
<span data-ttu-id="8fd85-109">Polecenie cmdlet **Remove-AzNetAppFilesAccount** usuwa konto ANF.</span><span class="sxs-lookup"><span data-stu-id="8fd85-109">The **Remove-AzNetAppFilesAccount** cmdlet deletes an ANF account.</span></span>

## <span data-ttu-id="8fd85-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8fd85-110">EXAMPLES</span></span>

### <span data-ttu-id="8fd85-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8fd85-111">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesAccount -ResourceGroupName "MyRG" -Name "MyAnfAccount"
```

<span data-ttu-id="8fd85-112">To polecenie usuwa konto ANF "MyAnfAccount".</span><span class="sxs-lookup"><span data-stu-id="8fd85-112">This command deletes the ANF account "MyAnfAccount".</span></span>

## <span data-ttu-id="8fd85-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8fd85-113">PARAMETERS</span></span>

### <span data-ttu-id="8fd85-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fd85-114">-DefaultProfile</span></span>
<span data-ttu-id="8fd85-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8fd85-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fd85-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="8fd85-116">-InputObject</span></span>
<span data-ttu-id="8fd85-117">Obiekt konta do usunięcia</span><span class="sxs-lookup"><span data-stu-id="8fd85-117">The account object to remove</span></span>

```yaml
Type: PSNetAppFilesAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8fd85-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8fd85-118">-Name</span></span>
<span data-ttu-id="8fd85-119">Nazwa konta usługi ANF</span><span class="sxs-lookup"><span data-stu-id="8fd85-119">The name of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fd85-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8fd85-120">-PassThru</span></span>
<span data-ttu-id="8fd85-121">Zwracanie, czy określone konto zostało pomyślnie usunięte</span><span class="sxs-lookup"><span data-stu-id="8fd85-121">Return whether the specified account was successfully removed</span></span>

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

### <span data-ttu-id="8fd85-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8fd85-122">-ResourceGroupName</span></span>
<span data-ttu-id="8fd85-123">Grupa zasobów konta ANF</span><span class="sxs-lookup"><span data-stu-id="8fd85-123">The resource group of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fd85-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8fd85-124">-ResourceId</span></span>
<span data-ttu-id="8fd85-125">Identyfikator zasobu konta ANF</span><span class="sxs-lookup"><span data-stu-id="8fd85-125">The resource id of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fd85-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8fd85-126">-Confirm</span></span>
<span data-ttu-id="8fd85-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8fd85-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8fd85-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8fd85-128">-WhatIf</span></span>
<span data-ttu-id="8fd85-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8fd85-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8fd85-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8fd85-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8fd85-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fd85-131">CommonParameters</span></span>
<span data-ttu-id="8fd85-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8fd85-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="8fd85-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8fd85-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fd85-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8fd85-134">INPUTS</span></span>

### <span data-ttu-id="8fd85-135">System. String</span><span class="sxs-lookup"><span data-stu-id="8fd85-135">System.String</span></span>

### <span data-ttu-id="8fd85-136">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="8fd85-136">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="8fd85-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8fd85-137">OUTPUTS</span></span>

### <span data-ttu-id="8fd85-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8fd85-138">System.Boolean</span></span>

## <span data-ttu-id="8fd85-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8fd85-139">NOTES</span></span>

## <span data-ttu-id="8fd85-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8fd85-140">RELATED LINKS</span></span>
