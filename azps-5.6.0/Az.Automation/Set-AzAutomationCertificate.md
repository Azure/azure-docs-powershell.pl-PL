---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: F1A2861F-14EF-4F67-8452-31FD498528BB
online version: https://docs.microsoft.com/powershell/module/az.automation/set-azautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationCertificate.md
ms.openlocfilehash: 80a33fe4664e4c7814db6774e7cd427dd9a2c87e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957729"
---
# <span data-ttu-id="f091d-101">Set-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="f091d-101">Set-AzAutomationCertificate</span></span>

## <span data-ttu-id="f091d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f091d-102">SYNOPSIS</span></span>
<span data-ttu-id="f091d-103">Modyfikuje konfigurację certyfikatu automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="f091d-103">Modifies the configuration of an Automation certificate.</span></span>

## <span data-ttu-id="f091d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f091d-104">SYNTAX</span></span>

```
Set-AzAutomationCertificate [-Name] <String> [-Description <String>] [-Password <SecureString>]
 [-Path <String>] [-Exportable <Boolean>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f091d-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="f091d-105">DESCRIPTION</span></span>
<span data-ttu-id="f091d-106">Polecenie **cmdlet Set-AzAutomationCertificate** modyfikuje konfigurację certyfikatu w usłudze Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="f091d-106">The **Set-AzAutomationCertificate** cmdlet modifies the configuration of a certificate in Azure Automation.</span></span>

## <span data-ttu-id="f091d-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f091d-107">EXAMPLES</span></span>

### <span data-ttu-id="f091d-108">Przykład 1. Modyfikowanie certyfikatu</span><span class="sxs-lookup"><span data-stu-id="f091d-108">Example 1: Modify a certificate</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String "Password" -AsPlainText -Force
PS C:\> Set-AzAutomationCertificate -AutomationAccountName "Contos17" -Name "ContosoCertificate" -Path "./cert.pfx" -Password $Password -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="f091d-109">Pierwsze polecenie konwertuje hasło w formacie zwykłego tekstu na bezpieczny ciąg za pomocą ConvertTo-SecureString cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f091d-109">The first command converts a plain text password to be a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="f091d-110">Polecenie przechowuje ten obiekt w $Password zmienną.</span><span class="sxs-lookup"><span data-stu-id="f091d-110">The command stores that object in the $Password variable.</span></span>
<span data-ttu-id="f091d-111">Drugie polecenie modyfikuje certyfikat o nazwie ContosoCertificate.</span><span class="sxs-lookup"><span data-stu-id="f091d-111">The second command modifies a certificate named ContosoCertificate.</span></span>
<span data-ttu-id="f091d-112">To polecenie używa hasła przechowywanego w $Password.</span><span class="sxs-lookup"><span data-stu-id="f091d-112">The command uses the password stored in $Password.</span></span>
<span data-ttu-id="f091d-113">To polecenie określa nazwę konta i ścieżkę do pliku, który jest przesyłany.</span><span class="sxs-lookup"><span data-stu-id="f091d-113">The command specifies the account name and the path of the file that it uploads.</span></span>

## <span data-ttu-id="f091d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f091d-114">PARAMETERS</span></span>

### <span data-ttu-id="f091d-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f091d-115">-AutomationAccountName</span></span>
<span data-ttu-id="f091d-116">Określa nazwę konta automatyzacji, dla którego to polecenie cmdlet modyfikuje certyfikat.</span><span class="sxs-lookup"><span data-stu-id="f091d-116">Specifies the name of the Automation account for which this cmdlet modifies a certificate.</span></span>

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

### <span data-ttu-id="f091d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f091d-117">-DefaultProfile</span></span>
<span data-ttu-id="f091d-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="f091d-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f091d-119">— Opis</span><span class="sxs-lookup"><span data-stu-id="f091d-119">-Description</span></span>
<span data-ttu-id="f091d-120">Określa opis certyfikatu, który zostanie zmodyfikowany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f091d-120">Specifies a description for the certificate that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f091d-121">-Exportable</span><span class="sxs-lookup"><span data-stu-id="f091d-121">-Exportable</span></span>
<span data-ttu-id="f091d-122">Określa, czy certyfikat można wyeksportować.</span><span class="sxs-lookup"><span data-stu-id="f091d-122">Specifies whether the certificate can be exported.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f091d-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="f091d-123">-Name</span></span>
<span data-ttu-id="f091d-124">Określa nazwę certyfikatu, który zostanie zmodyfikowany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f091d-124">Specifies the name of the certificate that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f091d-125">— Hasło</span><span class="sxs-lookup"><span data-stu-id="f091d-125">-Password</span></span>
<span data-ttu-id="f091d-126">Określa hasło pliku certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="f091d-126">Specifies the password for the certificate file.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f091d-127">— Ścieżka</span><span class="sxs-lookup"><span data-stu-id="f091d-127">-Path</span></span>
<span data-ttu-id="f091d-128">Określa ścieżkę do pliku skryptu do przekazania.</span><span class="sxs-lookup"><span data-stu-id="f091d-128">Specifies the path to a script file to upload.</span></span>
<span data-ttu-id="f091d-129">Plik może być plikiem cer lub plikiem pfx.</span><span class="sxs-lookup"><span data-stu-id="f091d-129">The file can be a .cer file or a .pfx file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f091d-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f091d-130">-ResourceGroupName</span></span>
<span data-ttu-id="f091d-131">Określa nazwę grupy zasobów, dla której to polecenie cmdlet modyfikuje certyfikat.</span><span class="sxs-lookup"><span data-stu-id="f091d-131">Specifies the name of the resource group for which this cmdlet modifies a certificate.</span></span>

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

### <span data-ttu-id="f091d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f091d-132">CommonParameters</span></span>
<span data-ttu-id="f091d-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f091d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f091d-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f091d-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f091d-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f091d-135">INPUTS</span></span>

### <span data-ttu-id="f091d-136">System.String</span><span class="sxs-lookup"><span data-stu-id="f091d-136">System.String</span></span>

### <span data-ttu-id="f091d-137">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="f091d-137">System.Security.SecureString</span></span>

### <span data-ttu-id="f091d-138">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="f091d-138">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="f091d-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f091d-139">OUTPUTS</span></span>

### <span data-ttu-id="f091d-140">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="f091d-140">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="f091d-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f091d-141">NOTES</span></span>

## <span data-ttu-id="f091d-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f091d-142">RELATED LINKS</span></span>

[<span data-ttu-id="f091d-143">Get-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="f091d-143">Get-AzAutomationCertificate</span></span>](./Get-AzAutomationCertificate.md)

[<span data-ttu-id="f091d-144">New-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="f091d-144">New-AzAutomationCertificate</span></span>](./New-AzAutomationCertificate.md)

[<span data-ttu-id="f091d-145">Remove-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="f091d-145">Remove-AzAutomationCertificate</span></span>](./Remove-AzAutomationCertificate.md)


