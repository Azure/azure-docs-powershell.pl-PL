---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 415C5854-FE03-4D4E-BE84-408EA5F95E34
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/set-azdatalakestoreitemowner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemOwner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemOwner.md
ms.openlocfilehash: 37dbb1c81de0f7537dd708dc39b2356edfa46f6b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995597"
---
# <span data-ttu-id="5d2ce-101">Set-AzDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="5d2ce-101">Set-AzDataLakeStoreItemOwner</span></span>

## <span data-ttu-id="5d2ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d2ce-102">SYNOPSIS</span></span>
<span data-ttu-id="5d2ce-103">Modyfikuje właściciela pliku lub folderu w sklepie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="5d2ce-103">Modifies the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="5d2ce-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5d2ce-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreItemOwner [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Type] <Owner>
 [-Id] <Guid> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5d2ce-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="5d2ce-105">DESCRIPTION</span></span>
<span data-ttu-id="5d2ce-106">Polecenie **cmdlet Set-AzDataLakeStoreItemOwner** modyfikuje właściciela pliku lub folderu w magazynie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="5d2ce-106">The **Set-AzDataLakeStoreItemOwner** cmdlet modifies the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="5d2ce-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5d2ce-107">EXAMPLES</span></span>

### <span data-ttu-id="5d2ce-108">Przykład 1. Ustawianie właściciela elementu</span><span class="sxs-lookup"><span data-stu-id="5d2ce-108">Example 1: Set the owner for an item</span></span>
```
PS C:\>Set-AzDataLakeStoreItemOwner -AccountName "ContosoADL" -Path / -Type User -Id (Get-AzADUser -Mail "PattiFuller@contoso.com").ObjectId
```

<span data-ttu-id="5d2ce-109">To polecenie ustawia właściciela katalogu głównego na Patti Fuller.</span><span class="sxs-lookup"><span data-stu-id="5d2ce-109">This command sets the owner for the root directory to Patti Fuller.</span></span>

## <span data-ttu-id="5d2ce-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5d2ce-110">PARAMETERS</span></span>

### <span data-ttu-id="5d2ce-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="5d2ce-111">-Account</span></span>
<span data-ttu-id="5d2ce-112">Określa nazwę konta sklepu Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="5d2ce-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="5d2ce-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d2ce-113">-DefaultProfile</span></span>
<span data-ttu-id="5d2ce-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="5d2ce-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5d2ce-115">— Identyfikator</span><span class="sxs-lookup"><span data-stu-id="5d2ce-115">-Id</span></span>
<span data-ttu-id="5d2ce-116">Określa identyfikator obiektu użytkownika, grupy lub podmiotu zabezpieczeń usługi AzureActive Directory, który ma być właścicielem.</span><span class="sxs-lookup"><span data-stu-id="5d2ce-116">Specifies the object ID of the AzureActive Directory user, group, or service principal to use as the owner.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d2ce-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5d2ce-117">-PassThru</span></span>
<span data-ttu-id="5d2ce-118">Wskazuje, że wynikowa aktualizacja właściciela powinna zostać zwrócona.</span><span class="sxs-lookup"><span data-stu-id="5d2ce-118">Indicates the resulting updated owner should be returned.</span></span>

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

### <span data-ttu-id="5d2ce-119">— Ścieżka</span><span class="sxs-lookup"><span data-stu-id="5d2ce-119">-Path</span></span>
<span data-ttu-id="5d2ce-120">Określa ścieżkę elementu do zmodyfikowania w sklepie Data Lake Store, zaczynając od katalogu głównego (/).</span><span class="sxs-lookup"><span data-stu-id="5d2ce-120">Specifies the Data Lake Store path of the item to modify, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="5d2ce-121">— Wpisz</span><span class="sxs-lookup"><span data-stu-id="5d2ce-121">-Type</span></span>
<span data-ttu-id="5d2ce-122">Określa typ właściciela, który ma być ustawiany.</span><span class="sxs-lookup"><span data-stu-id="5d2ce-122">Specifies the type of owner to set.</span></span>
<span data-ttu-id="5d2ce-123">Dopuszczalne wartości dla tego parametru to: Użytkownik i Grupa.</span><span class="sxs-lookup"><span data-stu-id="5d2ce-123">The acceptable values for this parameter are: User and Group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Owner
Parameter Sets: (All)
Aliases:
Accepted values: User, Group

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d2ce-124">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5d2ce-124">-Confirm</span></span>
<span data-ttu-id="5d2ce-125">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="5d2ce-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d2ce-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d2ce-126">-WhatIf</span></span>
<span data-ttu-id="5d2ce-127">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5d2ce-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d2ce-128">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="5d2ce-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d2ce-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d2ce-129">CommonParameters</span></span>
<span data-ttu-id="5d2ce-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d2ce-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d2ce-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d2ce-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d2ce-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5d2ce-132">INPUTS</span></span>

### <span data-ttu-id="5d2ce-133">System.String</span><span class="sxs-lookup"><span data-stu-id="5d2ce-133">System.String</span></span>

### <span data-ttu-id="5d2ce-134">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="5d2ce-134">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="5d2ce-135">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Właściciel</span><span class="sxs-lookup"><span data-stu-id="5d2ce-135">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Owner</span></span>

### <span data-ttu-id="5d2ce-136">System.Guid</span><span class="sxs-lookup"><span data-stu-id="5d2ce-136">System.Guid</span></span>

### <span data-ttu-id="5d2ce-137">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="5d2ce-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="5d2ce-138">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5d2ce-138">OUTPUTS</span></span>

### <span data-ttu-id="5d2ce-139">System.String</span><span class="sxs-lookup"><span data-stu-id="5d2ce-139">System.String</span></span>

## <span data-ttu-id="5d2ce-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5d2ce-140">NOTES</span></span>

## <span data-ttu-id="5d2ce-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5d2ce-141">RELATED LINKS</span></span>

[<span data-ttu-id="5d2ce-142">Get-AzDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="5d2ce-142">Get-AzDataLakeStoreItemOwner</span></span>](./Get-AzDataLakeStoreItemOwner.md)


