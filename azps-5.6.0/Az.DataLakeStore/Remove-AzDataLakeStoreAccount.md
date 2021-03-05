---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 585D6C4D-EA80-4E6B-8C36-E7632430431F
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/remove-azdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreAccount.md
ms.openlocfilehash: 8bb60e46f6785b29f8c2d64aadcce4d8697f4e16
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991411"
---
# <span data-ttu-id="c418a-101">Remove-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="c418a-101">Remove-AzDataLakeStoreAccount</span></span>

## <span data-ttu-id="c418a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c418a-102">SYNOPSIS</span></span>
<span data-ttu-id="c418a-103">Trwale usuwa konto w sklepie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c418a-103">Deletes a Data Lake Store account permanently.</span></span>

## <span data-ttu-id="c418a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c418a-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreAccount [-Name] <String> [[-ResourceGroupName] <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c418a-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="c418a-105">DESCRIPTION</span></span>
<span data-ttu-id="c418a-106">Polecenie **cmdlet Remove-AzDataLakeStoreAccount** trwale usuwa konto w sklepie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c418a-106">The **Remove-AzDataLakeStoreAccount** cmdlet deletes a Data Lake Store account permanently.</span></span>

## <span data-ttu-id="c418a-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c418a-107">EXAMPLES</span></span>

### <span data-ttu-id="c418a-108">Przykład 1. Usuwanie konta w sklepie Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="c418a-108">Example 1: Remove a Data Lake Store account</span></span>
```
PS C:\>Remove-AzDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="c418a-109">To polecenie usuwa konto o nazwie ContosoADL z magazynu Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c418a-109">This command removes the account named ContosoADL from the Data Lake Store.</span></span>

## <span data-ttu-id="c418a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c418a-110">PARAMETERS</span></span>

### <span data-ttu-id="c418a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c418a-111">-DefaultProfile</span></span>
<span data-ttu-id="c418a-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="c418a-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c418a-113">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="c418a-113">-Force</span></span>
<span data-ttu-id="c418a-114">Wymusza uruchomienie polecenia bez pytania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="c418a-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c418a-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="c418a-115">-Name</span></span>
<span data-ttu-id="c418a-116">Określa nazwę konta do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="c418a-116">Specifies the name of the account to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c418a-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c418a-117">-PassThru</span></span>
<span data-ttu-id="c418a-118">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="c418a-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c418a-119">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="c418a-119">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c418a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c418a-120">-ResourceGroupName</span></span>
<span data-ttu-id="c418a-121">Określa grupę zasobów zawierającą konto do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="c418a-121">Specifies the resource group that contains the account to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c418a-122">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c418a-122">-Confirm</span></span>
<span data-ttu-id="c418a-123">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c418a-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c418a-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c418a-124">-WhatIf</span></span>
<span data-ttu-id="c418a-125">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c418a-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c418a-126">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="c418a-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c418a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c418a-127">CommonParameters</span></span>
<span data-ttu-id="c418a-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c418a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c418a-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c418a-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c418a-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c418a-130">INPUTS</span></span>

### <span data-ttu-id="c418a-131">System.String</span><span class="sxs-lookup"><span data-stu-id="c418a-131">System.String</span></span>

## <span data-ttu-id="c418a-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c418a-132">OUTPUTS</span></span>

### <span data-ttu-id="c418a-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c418a-133">System.Boolean</span></span>

## <span data-ttu-id="c418a-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c418a-134">NOTES</span></span>

## <span data-ttu-id="c418a-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c418a-135">RELATED LINKS</span></span>

[<span data-ttu-id="c418a-136">Get-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="c418a-136">Get-AzDataLakeStoreAccount</span></span>](./Get-AzDataLakeStoreAccount.md)

[<span data-ttu-id="c418a-137">New-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="c418a-137">New-AzDataLakeStoreAccount</span></span>](./New-AzDataLakeStoreAccount.md)

[<span data-ttu-id="c418a-138">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="c418a-138">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)

[<span data-ttu-id="c418a-139">Test-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="c418a-139">Test-AzDataLakeStoreAccount</span></span>](./Test-AzDataLakeStoreAccount.md)


