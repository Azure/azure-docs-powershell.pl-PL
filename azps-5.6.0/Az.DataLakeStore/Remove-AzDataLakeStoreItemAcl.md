---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: D3E8A6A6-C6C5-46B0-914B-75088A6F6011
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/remove-azdatalakestoreitemacl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItemAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItemAcl.md
ms.openlocfilehash: 9b762a2fe0f12483fd664b8862e483b1b948bc75
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971130"
---
# <span data-ttu-id="e494f-101">Remove-AzDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="e494f-101">Remove-AzDataLakeStoreItemAcl</span></span>

## <span data-ttu-id="e494f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e494f-102">SYNOPSIS</span></span>
<span data-ttu-id="e494f-103">Wyczyszczenie listy ACL pliku lub folderu w sklepie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e494f-103">Clears the ACL of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="e494f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e494f-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreItemAcl [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Default] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e494f-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="e494f-105">DESCRIPTION</span></span>
<span data-ttu-id="e494f-106">Polecenie **cmdlet Remove-AzDataLakeStoreItemAcl** powoduje wyczyszczenie listy kontroli dostępu (ACL) pliku lub folderu w magazynie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e494f-106">The **Remove-AzDataLakeStoreItemAcl** cmdlet clears the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="e494f-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e494f-107">EXAMPLES</span></span>

### <span data-ttu-id="e494f-108">Przykład 1. Usuwanie listy ACL z folderu</span><span class="sxs-lookup"><span data-stu-id="e494f-108">Example 1: Remove the ACL from a folder</span></span>
```
PS C:\>Remove-AzDataLakeStoreItemAcl -AccountName "ContosoADL" -Path "/"
```

<span data-ttu-id="e494f-109">To polecenie usuwa acl dla katalogu głównego dla konta ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="e494f-109">This command removes the ACL for the root directory for the ContosoADL account.</span></span>

## <span data-ttu-id="e494f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e494f-110">PARAMETERS</span></span>

### <span data-ttu-id="e494f-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="e494f-111">-Account</span></span>
<span data-ttu-id="e494f-112">Określa nazwę konta w sklepie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e494f-112">Specifies the Data Lake Store account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e494f-113">— Domyślne</span><span class="sxs-lookup"><span data-stu-id="e494f-113">-Default</span></span>
<span data-ttu-id="e494f-114">Wskazuje, że polecenie cmdlet usuwa domyślną wartość ACL dla pliku lub folderu.</span><span class="sxs-lookup"><span data-stu-id="e494f-114">Indicates that the cmdlet removes the default ACL for a file or a folder.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e494f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e494f-115">-DefaultProfile</span></span>
<span data-ttu-id="e494f-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e494f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e494f-117">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="e494f-117">-Force</span></span>
<span data-ttu-id="e494f-118">Wymusza uruchomienie polecenia bez pytania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="e494f-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e494f-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e494f-119">-PassThru</span></span>
<span data-ttu-id="e494f-120">Wskazuje, że powinna zostać zwrócona odpowiedź logiczna wskazująca wynik operacji usuwania.</span><span class="sxs-lookup"><span data-stu-id="e494f-120">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e494f-121">— Ścieżka</span><span class="sxs-lookup"><span data-stu-id="e494f-121">-Path</span></span>
<span data-ttu-id="e494f-122">Określa ścieżkę elementu do magazynu Data Lake Store, rozpoczynając od katalogu głównego (/).</span><span class="sxs-lookup"><span data-stu-id="e494f-122">Specifies the Data Lake Store path of the item, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e494f-123">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e494f-123">-Confirm</span></span>
<span data-ttu-id="e494f-124">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e494f-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e494f-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e494f-125">-WhatIf</span></span>
<span data-ttu-id="e494f-126">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e494f-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e494f-127">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e494f-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e494f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e494f-128">CommonParameters</span></span>
<span data-ttu-id="e494f-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e494f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e494f-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e494f-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e494f-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e494f-131">INPUTS</span></span>

### <span data-ttu-id="e494f-132">System.String</span><span class="sxs-lookup"><span data-stu-id="e494f-132">System.String</span></span>

### <span data-ttu-id="e494f-133">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="e494f-133">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="e494f-134">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="e494f-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e494f-135">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e494f-135">OUTPUTS</span></span>

### <span data-ttu-id="e494f-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e494f-136">System.Boolean</span></span>

## <span data-ttu-id="e494f-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e494f-137">NOTES</span></span>
* <span data-ttu-id="e494f-138">Alias: Remove-AdlStoreAcl</span><span class="sxs-lookup"><span data-stu-id="e494f-138">Alias: Remove-AdlStoreAcl</span></span>

## <span data-ttu-id="e494f-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e494f-139">RELATED LINKS</span></span>

[<span data-ttu-id="e494f-140">Get-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="e494f-140">Get-AzDataLakeStoreItemAclEntry</span></span>](./Get-AzDataLakeStoreItemAclEntry.md)

[<span data-ttu-id="e494f-141">Set-AzDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="e494f-141">Set-AzDataLakeStoreItemAcl</span></span>](./Set-AzDataLakeStoreItemAcl.md)

[<span data-ttu-id="e494f-142">Set-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="e494f-142">Set-AzDataLakeStoreItemAclEntry</span></span>](./Set-AzDataLakeStoreItemAclEntry.md)


