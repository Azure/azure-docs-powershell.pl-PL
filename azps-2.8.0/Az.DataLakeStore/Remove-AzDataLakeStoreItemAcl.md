---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: D3E8A6A6-C6C5-46B0-914B-75088A6F6011
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/remove-azdatalakestoreitemacl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItemAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItemAcl.md
ms.openlocfilehash: 9339857a125ca0646869a81749f9cf55ff2531ee
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705787"
---
# <span data-ttu-id="ab4ed-101">Remove-AzDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="ab4ed-101">Remove-AzDataLakeStoreItemAcl</span></span>

## <span data-ttu-id="ab4ed-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ab4ed-102">SYNOPSIS</span></span>
<span data-ttu-id="ab4ed-103">Czyści listę ACL pliku lub folderu w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ab4ed-103">Clears the ACL of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="ab4ed-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ab4ed-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreItemAcl [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Default] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab4ed-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ab4ed-105">DESCRIPTION</span></span>
<span data-ttu-id="ab4ed-106">Polecenie cmdlet **Remove-AzDataLakeStoreItemAcl** czyści listę kontroli dostępu (ACL) pliku lub folderu w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ab4ed-106">The **Remove-AzDataLakeStoreItemAcl** cmdlet clears the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="ab4ed-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ab4ed-107">EXAMPLES</span></span>

### <span data-ttu-id="ab4ed-108">Przykład 1: Usuwanie listy ACL z folderu</span><span class="sxs-lookup"><span data-stu-id="ab4ed-108">Example 1: Remove the ACL from a folder</span></span>
```
PS C:\>Remove-AzDataLakeStoreItemAcl -AccountName "ContosoADL" -Path "/"
```

<span data-ttu-id="ab4ed-109">To polecenie usuwa listę ACL katalogu głównego dla konta usługi ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="ab4ed-109">This command removes the ACL for the root directory for the ContosoADL account.</span></span>

## <span data-ttu-id="ab4ed-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ab4ed-110">PARAMETERS</span></span>

### <span data-ttu-id="ab4ed-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="ab4ed-111">-Account</span></span>
<span data-ttu-id="ab4ed-112">Określa nazwę konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ab4ed-112">Specifies the Data Lake Store account name.</span></span>

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

### <span data-ttu-id="ab4ed-113">-Wartość domyślna</span><span class="sxs-lookup"><span data-stu-id="ab4ed-113">-Default</span></span>
<span data-ttu-id="ab4ed-114">Wskazuje, że polecenie cmdlet powoduje usunięcie domyślnego ACL pliku lub folderu.</span><span class="sxs-lookup"><span data-stu-id="ab4ed-114">Indicates that the cmdlet removes the default ACL for a file or a folder.</span></span>

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

### <span data-ttu-id="ab4ed-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab4ed-115">-DefaultProfile</span></span>
<span data-ttu-id="ab4ed-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ab4ed-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ab4ed-117">-Force</span><span class="sxs-lookup"><span data-stu-id="ab4ed-117">-Force</span></span>
<span data-ttu-id="ab4ed-118">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="ab4ed-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ab4ed-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ab4ed-119">-PassThru</span></span>
<span data-ttu-id="ab4ed-120">Wskazuje, że należy zwrócić odpowiedź logiczną wskazującą wynik operacji usuwania.</span><span class="sxs-lookup"><span data-stu-id="ab4ed-120">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="ab4ed-121">-Path</span><span class="sxs-lookup"><span data-stu-id="ab4ed-121">-Path</span></span>
<span data-ttu-id="ab4ed-122">Określa ścieżkę elementu Data Lake Store, rozpoczynając od katalogu głównego (/).</span><span class="sxs-lookup"><span data-stu-id="ab4ed-122">Specifies the Data Lake Store path of the item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="ab4ed-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ab4ed-123">-Confirm</span></span>
<span data-ttu-id="ab4ed-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab4ed-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab4ed-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab4ed-125">-WhatIf</span></span>
<span data-ttu-id="ab4ed-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab4ed-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab4ed-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ab4ed-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab4ed-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab4ed-128">CommonParameters</span></span>
<span data-ttu-id="ab4ed-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab4ed-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab4ed-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab4ed-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab4ed-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ab4ed-131">INPUTS</span></span>

### <span data-ttu-id="ab4ed-132">System. String</span><span class="sxs-lookup"><span data-stu-id="ab4ed-132">System.String</span></span>

### <span data-ttu-id="ab4ed-133">Microsoft. Azure. Commands. DataLakeStore. models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="ab4ed-133">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="ab4ed-134">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ab4ed-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ab4ed-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ab4ed-135">OUTPUTS</span></span>

### <span data-ttu-id="ab4ed-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ab4ed-136">System.Boolean</span></span>

## <span data-ttu-id="ab4ed-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ab4ed-137">NOTES</span></span>
* <span data-ttu-id="ab4ed-138">Alias: Remove-AdlStoreAcl</span><span class="sxs-lookup"><span data-stu-id="ab4ed-138">Alias: Remove-AdlStoreAcl</span></span>

## <span data-ttu-id="ab4ed-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ab4ed-139">RELATED LINKS</span></span>

[<span data-ttu-id="ab4ed-140">Get-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="ab4ed-140">Get-AzDataLakeStoreItemAclEntry</span></span>](./Get-AzDataLakeStoreItemAclEntry.md)

[<span data-ttu-id="ab4ed-141">Set-AzDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="ab4ed-141">Set-AzDataLakeStoreItemAcl</span></span>](./Set-AzDataLakeStoreItemAcl.md)

[<span data-ttu-id="ab4ed-142">Set-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="ab4ed-142">Set-AzDataLakeStoreItemAclEntry</span></span>](./Set-AzDataLakeStoreItemAclEntry.md)


