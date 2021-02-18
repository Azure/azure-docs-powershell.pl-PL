---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 1B29AB8C-95DD-4C4F-86E2-2F81E8020CEA
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageTable.md
ms.openlocfilehash: 98ffbfe7153ba0592563b21695e1a4d1c227f99a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190739"
---
# <span data-ttu-id="a6ae5-101">Remove-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="a6ae5-101">Remove-AzStorageTable</span></span>

## <span data-ttu-id="a6ae5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6ae5-102">SYNOPSIS</span></span>
<span data-ttu-id="a6ae5-103">Usuwa tabelę magazynu.</span><span class="sxs-lookup"><span data-stu-id="a6ae5-103">Removes a storage table.</span></span>

## <span data-ttu-id="a6ae5-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a6ae5-104">SYNTAX</span></span>

```
Remove-AzStorageTable [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6ae5-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="a6ae5-105">DESCRIPTION</span></span>
<span data-ttu-id="a6ae5-106">Polecenie **cmdlet Remove-AzStorageTable** usuwa jedną lub więcej tabel magazynu z konta magazynu na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="a6ae5-106">The **Remove-AzStorageTable** cmdlet removes one or more storage tables from a storage account in Azure.</span></span>

## <span data-ttu-id="a6ae5-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a6ae5-107">EXAMPLES</span></span>

### <span data-ttu-id="a6ae5-108">Przykład 1. Usuwanie tabeli</span><span class="sxs-lookup"><span data-stu-id="a6ae5-108">Example 1: Remove a table</span></span>
```
PS C:\>Remove-AzStorageTable -Name "TableABC"
```

<span data-ttu-id="a6ae5-109">To polecenie usuwa tabelę.</span><span class="sxs-lookup"><span data-stu-id="a6ae5-109">This command removes a table.</span></span>

### <span data-ttu-id="a6ae5-110">Przykład 2. Usuwanie kilku tabel</span><span class="sxs-lookup"><span data-stu-id="a6ae5-110">Example 2: Remove several tables</span></span>
```
PS C:\>Get-AzStorageTable table* | Remove-AzStorageTable
```

<span data-ttu-id="a6ae5-111">W tym przykładzie użyto symbolu wieloznacznego z parametrem *Name* w celu uzyskania wszystkich tabel, które pasują do tabeli wzorcowej, a następnie przekazuje wynik w potoku w celu usunięcia tabel.</span><span class="sxs-lookup"><span data-stu-id="a6ae5-111">This example uses a wildcard character with the *Name* parameter to get all tables that match the pattern table and then passes the result on the pipeline to remove the tables.</span></span>

## <span data-ttu-id="a6ae5-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a6ae5-112">PARAMETERS</span></span>

### <span data-ttu-id="a6ae5-113">— kontekst</span><span class="sxs-lookup"><span data-stu-id="a6ae5-113">-Context</span></span>
<span data-ttu-id="a6ae5-114">Określa kontekst magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a6ae5-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="a6ae5-115">Możesz go utworzyć za pomocą polecenia cmdlet New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6ae5-115">You can create it by using the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a6ae5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6ae5-116">-DefaultProfile</span></span>
<span data-ttu-id="a6ae5-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a6ae5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6ae5-118">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="a6ae5-118">-Force</span></span>
<span data-ttu-id="a6ae5-119">Wymusza uruchomienie polecenia bez pytania o potwierdzenie przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="a6ae5-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a6ae5-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a6ae5-120">-Name</span></span>
<span data-ttu-id="a6ae5-121">Określa nazwę tabeli do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="a6ae5-121">Specifies the name of the table to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Table

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a6ae5-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a6ae5-122">-PassThru</span></span>
<span data-ttu-id="a6ae5-123">Wskazuje, że to polecenie cmdlet zwraca **wartość** logiczną, która odzwierciedla sukces operacji.</span><span class="sxs-lookup"><span data-stu-id="a6ae5-123">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="a6ae5-124">Domyślnie to polecenie cmdlet nie zwraca wartości.</span><span class="sxs-lookup"><span data-stu-id="a6ae5-124">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="a6ae5-125">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a6ae5-125">-Confirm</span></span>
<span data-ttu-id="a6ae5-126">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a6ae5-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6ae5-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6ae5-127">-WhatIf</span></span>
<span data-ttu-id="a6ae5-128">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6ae5-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6ae5-129">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a6ae5-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6ae5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6ae5-130">CommonParameters</span></span>
<span data-ttu-id="a6ae5-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6ae5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6ae5-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6ae5-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6ae5-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a6ae5-133">INPUTS</span></span>

### <span data-ttu-id="a6ae5-134">System.String</span><span class="sxs-lookup"><span data-stu-id="a6ae5-134">System.String</span></span>

### <span data-ttu-id="a6ae5-135">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="a6ae5-135">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="a6ae5-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a6ae5-136">OUTPUTS</span></span>

### <span data-ttu-id="a6ae5-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a6ae5-137">System.Boolean</span></span>

## <span data-ttu-id="a6ae5-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a6ae5-138">NOTES</span></span>

## <span data-ttu-id="a6ae5-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a6ae5-139">RELATED LINKS</span></span>

[<span data-ttu-id="a6ae5-140">Get-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="a6ae5-140">Get-AzStorageTable</span></span>](./Get-AzStorageTable.md)
